---
title: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource Methode"
linktitle: "GetDataSource"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource method. Die Aspose.Words-Mail-Merge-Engine ruft diese Methode auf, wenn sie den Beginn einer Mail-Merge-Region auf oberster Ebene in C++ erkennt."
type: docs
weight: 2000
url: /de/cpp/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot::GetDataSource method


Die Aspose.Words Seriendruck-Engine ruft diese Methode auf, wenn sie den Beginn einer top‑level Seriendruckregion erkennt.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource(System::String tableName)=0
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| tableName | System::String | Der Name der Seriendruckregion, wie im Vorlagendokument angegeben. Case‑insensitive. |

### ReturnValue

Ein Datenquellenobjekt, das Zugriff auf die Datensätze der angegebenen Tabelle bietet.
## Hinweise


Wenn die Aspose.Words-Mail-Merge-Engine ein Dokument mit Daten füllt und auf MERGEFIELD TableStart:TableName trifft, ruft sie [GetDataSource()](./) für dieses Objekt auf. Ihre Implementierung muss ein neues Datenquellenobjekt zurückgeben. Aspose.Words wird die zurückgegebene Datenquelle verwenden, um die Mail-Merge-Region zu füllen.

Wenn eine Datenquelle (Tabelle) mit dem angegebenen Namen nicht existiert, sollte Ihre Implementierung **null** zurückgeben.

## Siehe auch

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Interface [IMailMergeDataSourceRoot](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
