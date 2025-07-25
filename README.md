# X12-837P-Claim-Mapping-Project

---

This project simulates a healthcare provider submitting a claim to a payer using the X12 837P format (005010X222A1). The goal is to parse raw EDI files using Boomi AtomSphere and map them into a structured JSON format for internal claim processing or validation.

---

## 🔧 Tools & Technologies
- **Boomi AtomSphere**
- **X12 837P (005010X222A1)**
- **HIPAA-compliant test data**
- **JSON transformation**
- **Document tracking**

---

## 📌 Project Features
- Configured X12 837P profile in Boomi using the 005010X222A1 schema
- Parsed subscriber information from NM1 segments (name, ID)
- Extracted claim details from CLM segment (claim ID, charge amount)
- Captured diagnosis codes from HI segment
- Mapped service line data from SV1 (procedure code and charge)
- Used Boomi's Document Tracking to test and validate claim mapping
---

## 🧪 Sample Output
```json
{
  "subscriber": {
    "first_name": "JOHN",
    "last_name": "DOE",
    "id": "123456789"
  },
  "claim": {
    "claim_id": "123456",
    "charge_amount": "400.00",
    "diagnosis_codes": ["R51", "M542"],
    "procedure_code": "99213",
    "procedure_charge": "150.00"
  }
}

```
### 🧠 Skills Demonstrated
* Healthcare EDI mapping fundamentals (837P)

* X12 segment/loop structure navigation

* JSON transformation logic

* Working with real EDI syntax

* Boomi document tracking and test data validation


## 🖼️ Mapping Preview

Below is a snapshot of the 837P to JSON mapping inside Boomi AtomSphere:

![Mapping Preview](files/map.png)





