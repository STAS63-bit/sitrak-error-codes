# Contributing / Как помочь

## Missing data / Недостающие данные

~209 error codes are missing FMI (Failure Mode Identifier) values. You can help!

### How to contribute

1. **Open an Issue** — [Create issue](https://github.com/STAS63-bit/sitrak-error-codes/issues/new?title=FMI+data:+SPN+___&labels=data-contribution) with:
   - SPN number
   - Correct FMI value
   - Source (service manual, diagnostic tool screenshot, etc.)

2. **Submit a Pull Request** — Edit `error-codes.json` directly:
   - Find the code with empty `fmi` field
   - Add the correct FMI value
   - Include source reference in PR description

### Data format

```json
{
  "spn": "0025",
  "fmi": "4",
  "dtc": "025-4",
  "description": "Fan drive malfunction",
  "description_ru": "Неисправность привода вентилятора",
  "system": "Bosch"
}
```

### Systems with missing FMI

| System | Missing |
|--------|---------|
| SCR | 60 |
| ZF_GearBox | 51 |
| HR_Radar | 45 |
| Bosch | 26 |
| WABCO_EBS31 | 17 |
| GPS | 8 |
| Other | 2 |

### Rules

- Only SAE J1939 standard data (SPN, FMI, DTC)
- No proprietary repair procedures
- Include source reference
- Russian translations welcome

---

*Maintained by [Мега Механика](https://megadata.pro)*
