---
title: "Aspose::Words::Settings::OdsoDataSourceType enum"
linktitle: "OdsoDataSourceType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Settings::OdsoDataSourceType enum. Anger typen av den externa datakällan som ska anslutas som en del av ODSO-anslutningsinformationen i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enum


Anger typen av den externa datakällan som ska anslutas till som en del av ODSO‑anslutningsinformationen.

```cpp
enum class OdsoDataSourceType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Text | 0 | Anger att ett givet dokument har anslutits till en textfil. Möjligtvis wdMergeSubTypeOther. |
| Database | 1 | Anger att ett givet dokument har anslutits till en databas. Möjligtvis wdMergeSubTypeAccess. |
| AddressBook | 2 | Anger att ett givet dokument har anslutits till en adressbok med kontakter. Möjligtvis wdMergeSubTypeOAL. |
| Document1 | 3 | Anger att ett givet dokument har anslutits till ett annat dokumentformat som stöds av den producerande applikationen. Möjligtvis wdMergeSubTypeOLEDBWord. |
| Document2 | 4 | Anger att ett givet dokument har anslutits till ett annat dokumentformat som stöds av den producerande applikationen. Möjligtvis wdMergeSubTypeWorks. |
| Native | 5 | Anger att ett givet dokument har anslutits till ett annat dokumentformat som är inbyggt i den producerande applikationen. Möjligtvis wdMergeSubTypeOLEDBText. |
| Email | 6 | Anger att ett givet dokument har anslutits till ett e-postprogram. Möjligtvis wdMergeSubTypeOutlook. |
| None | 7 | Typen av den externa datakällan är inte specificerad. Möjligtvis wdMergeSubTypeWord. |
| Legacy | 8 | Anger att ett givet dokument har anslutits till ett äldre dokumentformat som stöds av den producerande applikationen. Möjligtvis wdMergeSubTypeWord2000. |
| Master | 9 | Anger att ett givet dokument har anslutits till en datakälla som samlar andra datakällor. |
| Default | n/a | Motsvarar [None](./). |

## Anmärkningar


OOXML-specifikationen är mycket vag för den här uppräkningen. Jag antar att den kan motsvara WdMergeSubType-uppräkningen [http://msdn.microsoft.com/en-us/library/bb237801.aspx](http://msdn.microsoft.com/en-us/library/bb237801.aspx).

## Se även

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
