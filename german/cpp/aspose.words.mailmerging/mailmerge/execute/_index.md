---
title: "Aspose::Words::MailMerging::MailMerge::Execute Methode"
linktitle: "Ausführen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MailMerging::MailMerge::Execute Methode. Führt einen Mail‑Merge‑Vorgang für einen einzelnen Datensatz in C++ aus."
type: docs
weight: 3000
url: /de/cpp/aspose.words.mailmerging/mailmerge/execute/
---
## MailMerge::Execute(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) method


Führt einen Mail-Merge-Vorgang für einen einzelnen Datensatz durch.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::ArrayPtr<System::String> &fieldNames, const System::ArrayPtr<System::SharedPtr<System::Object>> &values)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fieldNames | const System::ArrayPtr\<System::String\>\& | Array von Merge‑Feldnamen. Feldnamen sind nicht case‑sensitive. Wenn ein Feldname, der im Dokument nicht gefunden wird, auftritt, wird er ignoriert. |
| values | const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\& | Array von Werten, die in die Merge‑Felder eingefügt werden sollen. Die Anzahl der Elemente in diesem Array muss mit der Anzahl der Elemente in *fieldNames* übereinstimmen. |
## Hinweise


Verwenden Sie diese Methode, um Mail‑Merge‑Felder im Dokument mit Werten aus einem Array von Objekten zu füllen.

Diese Methode führt Daten nur für einen einzelnen Datensatz zusammen. Das Array von Feldnamen und das Array von Werten stellen die Daten eines einzelnen Datensatzes dar.

Diese Methode verwendet keine Mail‑Merge‑Regionen.

Diese Methode ignoriert die Option [RemoveUnusedRegions](../../mailmergecleanupoptions/).

## Beispiele



Zeigt, wie ein Bild von einer URI als Mail‑Merge‑Daten in ein MERGEFIELD zusammengeführt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// MERGEFIELDs mit "Image:"‑Tags erhalten während eines Mail‑Merge ein Bild.
// Der String nach dem Doppelpunkt im "Image:"‑Tag entspricht einem Spaltennamen
// in der Datenquelle, deren Zellen URIs von Bilddateien enthalten.
builder->InsertField(u"MERGEFIELD  Image:logo_FromWeb ");
builder->InsertField(u"MERGEFIELD  Image:logo_FromFileSystem ");

// Erstellen Sie eine Datenquelle, die URIs von Bildern enthält, die wir zusammenführen.
// Eine URI kann eine Web‑URL sein, die auf ein Bild verweist, oder ein Dateiname einer Bilddatei im lokalen Dateisystem.
System::ArrayPtr<System::String> columns = System::MakeArray<System::String>({u"logo_FromWeb", u"logo_FromFileSystem"});
System::ArrayPtr<System::SharedPtr<System::Object>> URIs = System::MakeArray<System::SharedPtr<System::Object>>({System::ExplicitCast<System::Object>(get_ImageUrl()), System::ExplicitCast<System::Object>(get_ImageDir() + u"Logo.jpg")});

// Führen Sie einen Seriendruck auf einer Datenquelle mit einer Zeile aus.
doc->get_MailMerge()->Execute(columns, URIs);

doc->Save(get_ArtifactsDir() + u"MailMergeEvent.ImageFromUrl.docx");
```

## Siehe auch

* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::Execute(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Führt ein Mail-Merge aus einer benutzerdefinierten Datenquelle durch.

```cpp
void Aspose::Words::MailMerging::MailMerge::Execute(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | Ein Objekt, das die benutzerdefinierte Seriendruck‑Datenquellen‑Schnittstelle implementiert. |
## Hinweise


Verwenden Sie diese Methode, um Seriendruckfelder im Dokument mit Werten aus einer beliebigen Datenquelle wie einer Liste, Hashtable oder Objekten zu füllen. Sie müssen Ihre eigene Klasse schreiben, die die [IMailMergeDataSource](../../imailmergedatasource/)‑Schnittstelle implementiert.

Sie können diese Methode nur verwenden, wenn [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) **false** ist, das heißt, Sie benötigen keine Rechts‑nach‑Links‑Sprachkompatibilität (wie Arabisch oder Hebräisch).

Diese Methode ignoriert die Option [RemoveUnusedRegions](../../mailmergecleanupoptions/).

## Siehe auch

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
