# ICD10

The ICD 10 codes were retrieved from the CDC in June, 2015:
http://www.cdc.gov/nchs/icd/icd10cm.htm

The Chapter names were retrieved from the WHO in June, 2015:
http://apps.who.int/classifications/icd10/browse/2010/en

The IDs generated simply add 100000 to the row numbers provided by the CDC. The Chapters start at 200001, in order.

The ParentId column maps to the code's immediate parent.

The ChapterId, Cat3Id, Cat4Id, Cat5Id, and Cat6Id columns map to the chapter and code that is an ancestor of the given length.

This mapping is freely available, in the same way that the CDC and WHO provide their information freely.

Example rows:

|CDC2016Row|ICD10CodeId|ICD10Code|Len|NoChildren|Limited Description                                |Full Description                                   |Parent  |Chapter |Cat3|Cat4 |Cat5  |Cat6   |ParentId|ChapterId|Cat3Id |Cat4Id |Cat5Id |Cat6Id |
|----------|-----------|---------|---|----------|---------------------------------------------------|---------------------------------------------------|--------|--------|----|-----|------|-------|--------|---------|-------|-------|-------|-------|
|          |200000     |         |0  |0         |                                                   |                                                   |        |        |    |     |      |       |        |         |       |       |       |       |
|          |200007     |H00-H59  |2  |0         |Diseases of the eye and adnexa                     |Diseases of the eye and adnexa                     |        |        |    |     |      |       |200000  |         |       |       |       |       |
|08314     |108314     |H40      |3  |0         |Glaucoma                                           |Glaucoma                                           |H00-H59 |H00-H59 |    |     |      |       |200007  |200007   |       |       |       |       |
|08351     |108351     |H401     |4  |0         |Open-angle glaucoma                                |Open-angle glaucoma                                |H40     |H00-H59 |H40 |     |      |       |108314  |200007   |108314 |       |       |       |
|08364     |108364     |H4012    |5  |0         |Low-tension glaucoma                               |Low-tension glaucoma                               |H401    |H00-H59 |H40 |H401 |      |       |108351  |200007   |108314 |108351 |       |       |
|08365     |108365     |H40121   |6  |0         |Low-tension glaucoma, right eye                    |Low-tension glaucoma, right eye                    |H4012   |H00-H59 |H40 |H401 |H4012 |       |108364  |200007   |108314 |108351 |108364 |       |
|08366     |108366     |H401210  |7  |1         |Low-tension glaucoma, right eye, stage unspecified |Low-tension glaucoma, right eye, stage unspecified |H40121  |H00-H59 |H40 |H401 |H4012 |H40121 |108365  |200007   |108314 |108351 |108364 |108365 |

Dane Weber
2015-06-30