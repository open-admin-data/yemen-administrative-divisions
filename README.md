# Yemen Administrative Divisions / اليمن



## Overview

| Item | Details |
|------|---------|
| Governorate | 22 |
| District | 335 |
| Coordinates | ✅ Included (all levels) |
| Formats | JSON, NDJSON, CSV |
| License | CC-BY-4.0 |
| Last Updated | 2026-09-02 |
| Website | [openadmindata.org/ye](https://openadmindata.org/ye/) |
| API | [openadmindata.org/api/ye](https://openadmindata.org/api/ye/) |
| Flag | [PNG](https://onlygames.me/flags-png/ye/) · [CDN](https://www.freeflags.org/cdn/) · [CSS](https://www.freeflags.org/css/) · [Collections](https://www.freeflags.org/collections/) |
| National Anthem | [🎵 Listen & Download Yemen National Anthem MP3](https://onlygames.me/national-anthems/ye/) |

## Browse by Governorate

| # | Governorate | Districts | Link |
|---|----|----|------|
| 1 | ابين (Abyan) | 11 | [Browse](divisions/abyan-ye12/) |
| 2 | الضالع (Ad Dali&#39;) | 9 | [Browse](divisions/ad-dali-ye30/) |
| 3 | عدن (Aden) | 8 | [Browse](divisions/aden-ye24/) |
| 4 | البيضاء (Al Bayda) | 20 | [Browse](divisions/al-bayda-ye14/) |
| 5 | الحديده (Al Hodeidah) | 26 | [Browse](divisions/al-hodeidah-ye18/) |
| 6 | الجوف (Al Jawf) | 12 | [Browse](divisions/al-jawf-ye16/) |
| 7 | المهره (Al Maharah) | 9 | [Browse](divisions/al-maharah-ye28/) |
| 8 | المحويت (Al Mahwit) | 9 | [Browse](divisions/al-mahwit-ye27/) |
| 9 | عمران (Amran) | 20 | [Browse](divisions/amran-ye29/) |
| 10 | ذمار (Dhamar) | 12 | [Browse](divisions/dhamar-ye20/) |
| 11 | حضرموت (Hadramawt) | 28 | [Browse](divisions/hadramawt-ye19/) |
| 12 | حجه (Hajjah) | 31 | [Browse](divisions/hajjah-ye17/) |
| 13 | اب (Ibb) | 20 | [Browse](divisions/ibb-ye11/) |
| 14 | لحج (Lahj) | 15 | [Browse](divisions/lahj-ye25/) |
| 15 | مارب (Ma&#39;rib) | 14 | [Browse](divisions/marib-ye26/) |
| 16 | ريمه (Raymah) | 6 | [Browse](divisions/raymah-ye31/) |
| 17 | صعده (Sa&#39;dah) | 15 | [Browse](divisions/sadah-ye22/) |
| 18 | صنعاء (Sana&#39;a) | 16 | [Browse](divisions/sanaa-ye23/) |
| 19 | امانة العاصمه (Sana&#39;a City) | 12 | [Browse](divisions/sanaa-city-ye13/) |
| 20 | شبوه (Shabwah) | 17 | [Browse](divisions/shabwah-ye21/) |
| 21 | سقطرى (Socotra) | 2 | [Browse](divisions/socotra-ye32/) |
| 22 | تعز (Ta&#39;iz) | 23 | [Browse](divisions/taiz-ye15/) |

## Data Files

| File | Format | Description |
|------|--------|-------------|
| [all-governorate.json](data/all-governorate.json) | JSON | All 22 governorate records |
| [all-district.json](data/all-district.json) | JSON | All 335 district records |
| [all-flat.json](data/all-flat.json) | JSON | Levels 1-1 flat array |
| [all-flat.ndjson](data/all-flat.ndjson) | NDJSON | Streaming format |
| [all-flat.csv](data/all-flat.csv) | CSV | Spreadsheet format |
| [hierarchy.json](data/hierarchy.json) | JSON | Nested tree |
| [schema.json](data/schema.json) | JSON Schema | Data schema |

## Quick Start

### Python

```python
import json

with open("data/all-governorate.json", "r", encoding="utf-8") as f:
    data = json.load(f)

for r in data:
    print(f"{r['name']['local']} ({r['name']['en']}) — {r['children_count']['district']} districts")
```

### JavaScript

```javascript
import { readFileSync } from "fs";

const data = JSON.parse(readFileSync("data/all-governorate.json", "utf-8"));
console.log(`Total: ${data.length} governorates`);
```

## Schema

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique identifier |
| `level` | integer | 1=governorate, 2=district |
| `level_name` | object | Level label (local + English) |
| `name.local` | string | Name in local script |
| `name.en` | string | English name |
| `name.slug` | string | URL-safe slug |
| `parent` | object/null | Parent division reference |
| `ancestors` | array | Full ancestor chain |
| `children_count` | object | Count of children per level |
| `zip_codes` | array | Postal codes (where available) |
| `geo.lat` | string | Latitude (WGS84) |
| `geo.lon` | string | Longitude (WGS84) |

Full schema: [data/schema.json](data/schema.json)

## Hierarchy Browse

```
divisions/{governorate-slug}/
```

Districts are listed inline in each governorate's README.

## AI Integration

- [llms.txt](docs/llms.txt) — Quick reference for AI agents
- [llms-full.txt](docs/llms-full.txt) — Summary with per-governorate links
- [Per-governorate data](docs/llms-full/) — Full data by governorate

## Citation

```
Yemen Administrative Divisions Dataset (CC-BY-4.0)
URL: https://github.com/open-admin-data/yemen-administrative-divisions
```

See [CITATION.cff](CITATION.cff) for machine-readable citation.

## License

- **Data**: [CC-BY-4.0](LICENSE)

## Related

- [Open Admin Data](https://openadmindata.org) — Browse, search and explore administrative divisions for every country
- [open-admin-data](https://github.com/open-admin-data) — GitHub organization with all country repos
- [ListBase](https://www.listbase.org) — Structured reference data for every country
- [FreeFlags.org](https://www.freeflags.org) — Free flag images for every country
- [Flag CDN](https://www.freeflags.org/cdn/) — Hotlink flag images directly
- [Flag CSS](https://www.freeflags.org/css/) — CSS flag sprites for web projects
- [Flag Collections](https://www.freeflags.org/collections/) — Curated flag image packs
