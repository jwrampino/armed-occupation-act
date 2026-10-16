# armed-occupation-act 
*A Spatial History of the Armed Occupation Act of 1842* ([Overleaf Draft](https://www.overleaf.com/project/6ac98ed87517ad9581826c9d/share#45c76b703f4153953cf35a6a1c3698a2d680f85e72bdd25f))

### Repository Structure
```
armed-occupation-act/
├── data/                                           # Primary sources and extracted features
│   ├── SERIALSET-00507_00_00-009-0039-0000.pdf      # 1848 Abstract PDF
│   ├── SERIALSET-00507_00_00-009-0039-0000.txt      # 1848 Abstract TXT
│   └── SERIALSET-00507_00_00-009-0039-0000.json     # 1848 Abstract JSON (~structured tables)
├── ocr.ipynb                                       # OCR pipeline (HTR pipeline forthcoming)
├── environment.yml                                 # Conda stuff
└── README.md                                       # You are here
```

### Data

| Source | Gives | Status |
|---|---|---|
| [Covington (1961)](https://stars.library.ucf.edu/cgi/viewcontent.cgi?article=2786&context=fhq) and [DeSantis (2022)](https://stars.library.ucf.edu/fhq/vol101/iss2/4/) | Totals to reconcile against, historiography | Have |
| [1848 Commissioner's abstract, S. Ex. Doc. 30-39](https://www.govinfo.gov/app/details/SERIALSET-00507_00_00-009-0039-0000) | Per permit: permit and notice dates, settler, tract designation, carrier, family status, survey status, date, and designation, annulment or rejection reasons, sales, remarks | [Have](https://github.com/jwrampino/armed-occupation-act/blob/main/data/SERIALSET-00507_00_00-009-0039-0000.pdf) |
| [S. Ex. Doc. 30-38](https://www.govinfo.gov/app/details/SERIALSET-00507_00_00-008-0038-0000) | Bill-related Senate document | Dropped |
| [S. Misc. Doc. 30-74](https://www.govinfo.gov/app/details/SERIALSET-00511_00_00-075-0074-0000) and [H. Misc. Doc. 30-78](https://www.govinfo.gov/app/details/SERIALSET-00523_00_00-079-0078-0000) | Florida legislature resolutions on reverted lands and settlers' permits (aggregate abandonment evidence) | Not Reviewed |
| [DEP Land Document System](https://prodenv.dep.state.fl.us/DslBtlds/public/piSearchDocumentLoad), document type "AOP" | Original permit applications: full description, Florida residency date (handwritten) | Not Reviewed |
| [GLO Records (BLM)](https://glorecords.blm.gov/default.aspx) | Patents (completed claims), patent dates, legal descriptions | Not Reviewed |
| [DEP tract books](https://floridadep.gov/lands/bureau-survey-mapping/content/title-and-land-records) | Land sales 1824 to 1890, later ownership, reversion | Not Reviewed |
| [National Archives donation files](https://www.archives.gov/research/land/land-records) | Final proof of residence and cultivation (crops, acres, house, inhabitants) | Not Reviewed |
| PLSS geometry (check [LABINS](https://www.labins.org/survey_data/landrecords/landrecords.cfm)) | Township, range, and section polygons to place designations; no downloadable 1840s layer confirmed | Not Found |
| [Survey plats and field notes (LABINS)](https://www.labins.org/xtra_data/download/glo_instructions.pdf) | Timber, soil, water, and improvements along section lines (handwritten) | Not Reviewed |
| [Florida Seminole War Heritage Trail Heat Web Layer](https://www.arcgis.com/home/item.html?id=728ac370efa54e5e8ed91612265e7a89) | Forts, Seminole towns, battles, raids | Not Reviewed |
| Environmental layers (soils, hydrography, vegetation reconstruction) | Site-selection covariates | Not Found |
| 1840 and 1850 census | Demographics, name linkage | Not Found |
