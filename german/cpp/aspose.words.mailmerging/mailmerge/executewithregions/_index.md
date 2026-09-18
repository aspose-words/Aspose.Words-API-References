---
title: "Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions Methode"
linktitle: "ExecuteWithRegions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions Methode. Führt einen Mail‑Merge aus einer benutzerdefinierten Datenquelle mit Mail‑Merge‑Regionen in C++ durch."
type: docs
weight: 4000
url: /de/cpp/aspose.words.mailmerging/mailmerge/executewithregions/
---
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Führt ein Mail-Merge aus einer benutzerdefinierten Datenquelle mit Mail-Merge-Regionen durch.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | Ein Objekt, das die benutzerdefinierte Seriendruck‑Datenquellen‑Schnittstelle implementiert. |
## Hinweise


Verwenden Sie diese Methode, um Mail‑Merge‑Felder im Dokument mit Werten aus einer beliebigen benutzerdefinierten Datenquelle, wie einer XML‑Datei oder Sammlungen von Geschäftsobjekten, zu füllen. Sie müssen Ihre eigene Klasse schreiben, die das Interface [IMailMergeDataSource](../../imailmergedatasource/) implementiert.

Sie können diese Methode nur verwenden, wenn [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) **false** ist, das heißt, Sie benötigen keine Rechts‑nach‑Links‑Sprachkompatibilität (wie Arabisch oder Hebräisch).

## Siehe auch

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) method


Führt ein Mail-Merge aus einer benutzerdefinierten Datenquelle mit Mail-Merge-Regionen durch.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSourceRoot> &dataSourceRoot)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataSourceRoot | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\& | Ein Objekt, das das benutzerdefinierte Mail‑Merge‑Datenquellen‑Root‑Interface implementiert. |
## Hinweise


Verwenden Sie diese Methode, um Mail‑Merge‑Felder im Dokument mit Werten aus einer beliebigen benutzerdefinierten Datenquelle, wie einer XML‑Datei oder Sammlungen von Geschäftsobjekten, zu füllen. Sie müssen Ihre eigenen Klassen schreiben, die die Interfaces [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/) und [IMailMergeDataSource](../../imailmergedatasource/) implementieren.

Sie können diese Methode nur verwenden, wenn [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) **false** ist, das heißt, Sie benötigen keine Rechts‑nach‑Links‑Sprachkompatibilität (wie Arabisch oder Hebräisch).

## Siehe auch

* Interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
