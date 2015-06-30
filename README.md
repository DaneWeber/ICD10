# ICD10

The ICD 10 codes were retrieved from the CDC in June, 2015:
http://www.cdc.gov/nchs/icd/icd10cm.htm

The Chapter names were retrieved from the WHO in June, 2015:
http://apps.who.int/classifications/icd10/browse/2010/en

The IDs generated simply add 100000 to the row numbers provided by the CDC. The Chapters start at 200001, in order.

The ParentId column maps to the code's immediate parent.

The ChapterId, Cat3Id, Cat4Id, Cat5Id, and Cat6Id columns map to the chapter and code that is an ancestor of the given length.

This mapping is freely available, in the same way that the CDC and WHO provide their information freely.

Dane Weber
2015-06-30