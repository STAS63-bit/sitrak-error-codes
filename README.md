# SITRAK Error Codes Database / База кодов ошибок SITRAK

Открытая база кодов ошибок (DTC) для грузовиков SITRAK C7H, C9H, G7.

**7847 кодов** по 25+ системам: Bosch ECU, ZF TraXon, KNORR EBS, ECAS, ABS, NanoBCU, и другие.

## Формат данных

```json
{
  "spn": "520542",
  "fmi": "2",
  "dtc": "350",
  "description": "AGD switched to manual mode because ABS is not fully operational",
  "description_ru": "AGD переключен в ручной режим, потому что ABS не работает полностью",
  "system": "AMT"
}
```

| Поле | Описание |
|------|----------|
| `spn` | Suspect Parameter Number (стандарт SAE J1939) |
| `fmi` | Failure Mode Identifier |
| `dtc` | Diagnostic Trouble Code |
| `description` | Описание ошибки (EN) |
| `description_ru` | Описание ошибки (RU) |
| `system` | Блок управления / система |

## Системы

| Система | Кодов | Описание |
|---------|-------|----------|
| Bosch | 2257 | Двигатель MC11/MC13, EDC17 |
| KNORREBS | 1192 | Тормозная система KNORR EBS |
| OGP / OGP2 | 754 | Панель приборов |
| AMT | 430 | Коробка передач (ZF TraXon) |
| EBS | 357 | Электронная тормозная система |
| WABCO_EBS31 | 315 | WABCO EBS поколение 31 |
| ZF_GearBox | 301 | Коробка ZF |
| ABS / KNORRABS8 | 396 | Антиблокировочная система |
| ECAS / ECAS4PLUS | 295 | Пневмоподвеска |
| BCU / NanoBCU | 300+ | Блок управления кузовом |
| PCU | 163 | Блок управления мощностью |

## Использование

```python
import json

with open('error-codes.json', 'r', encoding='utf-8') as f:
    codes = json.load(f)

# Поиск по SPN
results = [c for c in codes if c.get('spn') == '520542']
```

```javascript
const codes = require('./error-codes.json');
const results = codes.filter(c => c.spn === '520542');
```

## Нужна помощь с диагностикой?

Эта база содержит описания ошибок. За рекомендациями по ремонту и диагностике обращайтесь:

- **Расшифровка онлайн:** [zmega.ru/codes](https://zmega.ru/codes/)
- **Мега Механика** — сервис грузовиков SITRAK: [megadata.pro](https://megadata.pro)
- **Telegram:** техподдержка для СТО

## Лицензия

Данные предоставлены на основе стандарта SAE J1939 и открытых спецификаций производителей.
Используйте свободно с указанием источника.

---

*Поддерживается [Мега Механика](https://megadata.pro) — сервис и запчасти SITRAK в России*
