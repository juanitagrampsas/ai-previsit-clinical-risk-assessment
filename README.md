# AI Pre-Visit Clinical Risk Assessment

A small n8n workflow project demonstrating how clinical data can be received, normalized, evaluated using conditional logic, and sent to another system through an API-style HTTP request.

## Project Overview

The workflow processes mock pre-visit patient data including:

- Patient ID and age
- Blood pressure
- Hemoglobin A1C
- Recent emergency visit

The incoming fields are mapped into a standardized structure. The workflow then evaluates the clinical data using conditional risk logic and identifies higher-risk patients.

For a higher-risk result, the workflow adds a `risk_level` value and sends the resulting structured JSON payload to an external endpoint using an HTTP POST request.

## Workflow

Input → Field Mapping → Data Normalization → Risk Logic → Risk Classification → HTTP POST

## Example Output

```json
{
  "patient_id": "Test-001",
  "patient_age": 67,
  "blood_pressure_systolic": 168,
  "hemoglobin_a1c": 8.4,
  "recent_emergency_visit": "YES",
  "blood_pressure_diastolic": 96,
  "risk_level": "HIGH"
}
```

## Tools & Concepts

n8n • JSON • HTTP/REST • Webhooks • Conditional Logic • Data Mapping • Healthcare Workflows

## Notes

This project uses mock patient data only and is intended as a technical portfolio demonstration. No real patient or protected health information (PHI) is used.
