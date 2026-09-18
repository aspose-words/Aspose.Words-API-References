---
title: "Aspose::Words::Settings::OdsoDataSourceType enum"
linktitle: "OdsoDataSourceType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Settings::OdsoDataSourceType enum. Gibt den Typ der externen Datenquelle an, die im Rahmen der ODSO-Verbindungsinformationen in C++ verbunden werden soll."
type: docs
weight: 19000
url: /de/cpp/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enum


Gibt den Typ der externen Datenquelle an, mit der im Rahmen der ODSO‑Verbindungsinformationen verbunden werden soll.

```cpp
enum class OdsoDataSourceType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Text | 0 | Gibt an, dass ein bestimmtes Dokument mit einer Textdatei verbunden wurde. Möglicherweise wdMergeSubTypeOther. |
| Database | 1 | Gibt an, dass ein bestimmtes Dokument mit einer Datenbank verbunden wurde. Möglicherweise wdMergeSubTypeAccess. |
| AddressBook | 2 | Gibt an, dass ein bestimmtes Dokument mit einem Adressbuch von Kontakten verbunden wurde. Möglicherweise wdMergeSubTypeOAL. |
| Document1 | 3 | Gibt an, dass ein bestimmtes Dokument mit einem anderen vom erzeugenden Programm unterstützten Dokumentformat verbunden wurde. Möglicherweise wdMergeSubTypeOLEDBWord. |
| Document2 | 4 | Gibt an, dass ein bestimmtes Dokument mit einem anderen vom erzeugenden Programm unterstützten Dokumentformat verbunden wurde. Möglicherweise wdMergeSubTypeWorks. |
| Native | 5 | Gibt an, dass ein bestimmtes Dokument mit einem anderen, dem erzeugenden Programm nativen Dokumentformat verbunden wurde. Möglicherweise wdMergeSubTypeOLEDBText. |
| Email | 6 | Gibt an, dass ein bestimmtes Dokument mit einer E‑Mail‑Anwendung verbunden wurde. Möglicherweise wdMergeSubTypeOutlook. |
| Keine | 7 | Der Typ der externen Datenquelle ist nicht angegeben. Möglicherweise wdMergeSubTypeWord. |
| Legacy | 8 | Gibt an, dass ein bestimmtes Dokument mit einem veralteten Dokumentformat, das vom erzeugenden Programm unterstützt wird, verbunden wurde. Möglicherweise wdMergeSubTypeWord2000. |
| Master | 9 | Gibt an, dass ein bestimmtes Dokument mit einer Datenquelle verbunden wurde, die andere Datenquellen aggregiert. |
| Default | n/a | Entspricht [None](./). |

## Hinweise


Die OOXML‑Spezifikation ist für diese Aufzählung sehr vage. Ich vermute, sie könnte der Aufzählung WdMergeSubType entsprechen [http://msdn.microsoft.com/en-us/library/bb237801.aspx](http://msdn.microsoft.com/en-us/library/bb237801.aspx).

## Siehe auch

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
