---
title: "Aspose::Words::MailMerging::FieldMergingArgs class"
linktitle: "FieldMergingArgs"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MailMerging::FieldMergingArgs Klasse. Stellt Daten für das MergeField-Ereignis bereit. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 1000
url: /de/cpp/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class


Stellt Daten für das **MergeField**-Ereignis bereit. Weitere Informationen finden Sie im Dokumentationsartikel [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class FieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Gibt das [Document](../fieldmergingargsbase/get_document/) Objekt zurück, für das der Seriendruck ausgeführt wird. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Ermittelt den Namen des Seriendruckfeldes, wie im Dokument angegeben. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Ermittelt das Objekt, das das aktuelle Seriendruckfeld darstellt. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Ermittelt den Namen des Seriendruckfeldes in der Datenquelle. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Ermittelt den Wert des Feldes aus der Datenquelle. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Ermittelt den nullbasierten Index des Datensatzes, der zusammengeführt wird. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Ermittelt den Namen der Datentabelle für die aktuelle Zusammenführungsoperation oder einen leeren String, wenn der Name nicht verfügbar ist. |
| [get_Text](./get_text/)() const | Ermittelt oder setzt den Text, der in das Dokument für das aktuelle Seriendruckfeld eingefügt wird. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Setzt den Wert des Feldes aus der Datenquelle. |
| [set_Text](./set_text/)(const System::String\&) | Setter für [Aspose::Words::MailMerging::FieldMergingArgs::get_Text](./get_text/). |
| static [Type](./type/)() |  |
## Hinweise


Das **MergeField**-Ereignis tritt während des Seriendrucks auf, wenn im Dokument ein einfaches Seriendruckfeld gefunden wird. Sie können auf dieses Ereignis reagieren, um Text zurückzugeben, den die Seriendruck-Engine in das Dokument einfügt.

## Siehe auch

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
