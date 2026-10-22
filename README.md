# armed-occupation-act 
*A Spatial History of the Armed Occupation Act of 1842*

| Contents |
|---|
| [Overleaf Draft](https://www.overleaf.com/project/6ac98ed87517ad9581826c9d/share#45c76b703f4153953cf35a6a1c3698a2d680f85e72bdd25f) |
| [RQ1](#where-did-claimants-settle) · [RQ2](#how-did-conflict-influence-abandonment-both-during-and-after-the-five-year-commitment) |
| [Repository Structure](#repository-structure) |
| [Data](#Data) |
| Methods |
| Results |
| Instructions |
| Job IDs |
| [Contextual Timeline](#contextual-timeline) |
| References |

### Research Questions

**Among Armed Occupation Act claimants, 1840–1860:**
- Where did claimants settle?
- How did conflict influence abandonment, both during and after the five-year commitment?

#### Where did claimants settle?
- **H1a:** Claims concentrate along interior travel routes and near water, relative to eligible unclaimed land.
- **H1b:** Claims over-select agriculturally productive land (hammock, old fields, good soil) relative to its availability, net of access.
- **H1c (competing):** Access to routes and water explains claim location better than land quality, as the "Actual Settler" letter alleges.

#### How did conflict influence abandonment, both during and after the five-year commitment?
- **H2a:** Claims closer to the Peace River Reservation were more likely to be abandoned.
- **H2b:** Claims farther from forts were abandoned more often than claims closer to forts.
- **H2c:** Claims in the interior south of Ocala show elevated abandonment after the 1849 scare.
- **H2d:** Claims with more neighbors who had already departed were more likely to be abandoned later, net of their own exposure to conflict.
- **H2e:** The effect of an attack on abandonment decays with Euclidean distance.
- **H2f (competing):** The effect spreads along the travel networks, and is better explained by network distance than by Euclidean distance.
- **H2g:** Agriculturally productive land buffers abandonment after conflict events.
- **H2h:** Completed claims in areas affected by later conflict episodes were abandoned more often than completed claims elsewhere.

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
| ["Actual Settler" letter, *Florida Republican*, May 9, 1850](https://ufdc.ufl.edu/UF00079922/00053) | Contemporary claim that settlers followed interior routes, bypassed rich hammock, and abandoned claims | Not Found |
| [Militia Muster Roles](https://floridamemory.com/discover/historical_records/muster_rolls/) and [Transcription](https://ufdc.ufl.edu/en/UF00047719/00011/images/0) ([Archive](https://archive.org/details/floridamilitiamu02morr))| Names, ages, ranks, and service dates. | Not Reviewed |
| Governor Thomas Brown letterbook, 1849-1853 ([Florida Memory](https://www.floridamemory.com/items/show/346026)) | 1849 correspondence | Not Reviewed |
| [GLO correspondence and 1844 agent reports on individual cases (NARA, RG 49)](https://www.archives.gov/research/guide-fed-records/groups/049.html) | Commissioner's letters to the Florida registers, and examining agent reports under the 1844 act: case-specific reasons for forfeitures, cancellations, and rejections | Not Found |
| [S. Misc. Doc. 30-74](https://www.govinfo.gov/app/details/SERIALSET-00511_00_00-075-0074-0000) and [H. Misc. Doc. 30-78](https://www.govinfo.gov/app/details/SERIALSET-00523_00_00-079-0078-0000) | Florida legislature resolutions on reverted lands and settlers' permits (aggregate abandonment evidence) | Not Reviewed |
| [DEP Land Document System](https://prodenv.dep.state.fl.us/DslBtlds/public/piSearchDocumentLoad), document type "AOP" | Original permit applications: full description, Florida residency date (handwritten) | Not Reviewed |
| [GLO Records (BLM)](https://glorecords.blm.gov/default.aspx) | Patents (completed claims), patent dates, legal descriptions | Not Reviewed |
| [DEP tract books](https://floridadep.gov/lands/bureau-survey-mapping/content/title-and-land-records) | Land sales 1824 to 1890, later ownership, reversion | Not Reviewed |
| [National Archives donation files](https://www.archives.gov/research/land/land-records) | Final proof of residence and cultivation (crops, acres, house, inhabitants) | Not Reviewed |
| [NARA M617: Returns from U.S. Military Posts, 1800-1916](https://www.archives.gov/files/research/microfilm/m617.pdf) | Troop movements | Not Reviewed |
| PLSS geometry (check [LABINS](https://www.labins.org/survey_data/landrecords/landrecords.cfm)) | Township, range, and section polygons to place designations; no downloadable 1840s layer confirmed | Not Found |
| [Survey plats and field notes (LABINS)](https://www.labins.org/xtra_data/download/glo_instructions.pdf) | Timber, soil, water, and improvements along section lines (handwritten) | Not Reviewed |
| [Florida Seminole War Heritage Trail Heat Web Layer](https://www.arcgis.com/home/item.html?id=728ac370efa54e5e8ed91612265e7a89) | Forts, Seminole towns, battles, raids | Not Reviewed |
| Environmental layers (soils, hydrography, vegetation reconstruction) | Site-selection covariates | Not Found |
| 1840, 1850 and 1860 census ([here](https://www.nhgis.org/) or [here](https://www.archives.gov/research/census/1850)) | Demographics, name linkage | Not Reviewed |

### **Contextual Timeline**

<details>
<summary>Expand timeline</summary>

| Event | Year | Era |
|---|---|---|
| Tecumseh's War | 1811-1813 | Background |
| War of 1812 | 1812-1815 | |
| Creek War (Red Stick War) | 1813-1814 | |
| Negro Fort Massacre | 1816 | |
| First Seminole War | 1816-1818 | |
| Adams-Onís Treaty | 1819-1821 | |
| Treaty of Moultrie Creek | 1823 | |
| Indian Removal Act | 1830 | |
| Nat Turner's Rebellion | 1831 | |
| Worcester v. Georgia | 1832 | |
| Black Hawk War | 1832 | |
| Treaty of Payne's Landing | 1832 | |
| Treaty of Fort Gibson | 1833 | |
| Dade Battle | 1835 | |
| Second Seminole War | 1835-1842 | |
| Forced Cherokee Removal | 1838 | |
| **Census of 1840** | 1840 | *Start of Inquiry* |
| Preemption Act | 1841 | |
| Armed Occupation Act | 1842 | |
| General Order 28 | 1842 | |
| Amendment to the Armed Occupation Act | 1844 | |
| Florida Statehood | 1845 | |
| Mexican-American War | 1846-1848 | |
| 1849 Seminole Raids ('Indian Scare of 1849') | 1849 | |
| Census of 1850 | 1850 | |
| Swamp Land Act | 1850 | |
| Graduation Act | 1854 | |
| Third Seminole War | 1855-1858 | |
| **Census of 1860** | 1860 | *End of Inquiry* |
| U.S. Civil War | 1861-1865 | |

</details>
  
  
##### [Back to Top](#armed-occupation-act)