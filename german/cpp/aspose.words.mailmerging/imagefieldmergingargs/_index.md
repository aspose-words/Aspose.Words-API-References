---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs class"
linktitle: "ImageFieldMergingArgs"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MailMerging::ImageFieldMergingArgs Klasse. Stellt Daten für das ImageFieldMerging()-Ereignis bereit. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.mailmerging/imagefieldmergingargs/
---
## ImageFieldMergingArgs class


Stellt Daten für das [ImageFieldMerging()](../ifieldmergingcallback/imagefieldmerging/) Ereignis bereit. Weitere Informationen finden Sie im [Mail Merge und Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/) Dokumentationsartikel.

```cpp
class ImageFieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Gibt das [Document](../fieldmergingargsbase/get_document/) Objekt zurück, für das der Seriendruck ausgeführt wird. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Ermittelt den Namen des Seriendruckfeldes, wie im Dokument angegeben. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Ermittelt das Objekt, das das aktuelle Seriendruckfeld darstellt. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Ermittelt den Namen des Seriendruckfeldes in der Datenquelle. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Ermittelt den Wert des Feldes aus der Datenquelle. |
| [get_Image](./get_image/)() const | Gibt das Bild an, das die Seriendruck-Engine in das Dokument einfügen muss. |
| [get_ImageFileName](./get_imagefilename/)() const | Legt den Dateinamen des Bildes fest, das die Seriendruck-Engine in das Dokument einfügen muss. |
| [get_ImageHeight](./get_imageheight/)() const | Gibt die Bildhöhe für das in das Dokument einzufügende Bild an. |
| [get_ImageStream](./get_imagestream/)() const | Gibt den Stream an, aus dem die Seriendruck-Engine ein Bild lesen soll. |
| [get_ImageWidth](./get_imagewidth/)() const | Gibt die Bildbreite für das in das Dokument einzufügende Bild an. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Ermittelt den nullbasierten Index des Datensatzes, der zusammengeführt wird. |
| [get_Shape](./get_shape/)() const | Gibt die Form an, die die Seriendruck-Engine in das Dokument einfügen muss. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Ermittelt den Namen der Datentabelle für die aktuelle Zusammenführungsoperation oder einen leeren String, wenn der Name nicht verfügbar ist. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Setzt den Wert des Feldes aus der Datenquelle. |
| [set_Image](./set_image/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Gibt das Bild an, das die Seriendruck-Engine in das Dokument einfügen muss. |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Legt den Dateinamen des Bildes fest, das die Seriendruck-Engine in das Dokument einfügen muss. |
| [set_ImageHeight](./set_imageheight/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | Setter für [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageHeight](./get_imageheight/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Gibt den Stream an, aus dem die Seriendruck-Engine ein Bild lesen soll. |
| [set_ImageStream](./set_imagestream/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [set_ImageWidth](./set_imagewidth/)(const System::SharedPtr\<Aspose::Words::Fields::MergeFieldImageDimension\>\&) | Setter für [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_ImageWidth](./get_imagewidth/). |
| [set_Shape](./set_shape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Setter für [Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape](./get_shape/). |
| static [Type](./type/)() |  |
## Hinweise


Dieses Ereignis tritt beim Seriendruck auf, wenn ein Bild-Seriendruckfeld im Dokument gefunden wird. Sie können auf dieses Ereignis reagieren, indem Sie einen Dateinamen, einen Stream oder ein **Image**‑Objekt an die Seriendruck-Engine zurückgeben, sodass es in das Dokument eingefügt wird.

Es stehen drei Eigenschaften zur Verfügung: [ImageFileName](./get_imagefilename/), [ImageStream](./get_imagestream/) und [Image](./get_image/), um anzugeben, woher das Bild genommen werden soll. Setzen Sie nur eine dieser Eigenschaften.

Um ein Bild-Seriendruckfeld in ein Word-Dokument einzufügen, wählen Sie den Befehl Einfügen/Feld, dann MergeField und geben Sie Image:MyFieldName ein.

## Siehe auch

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
