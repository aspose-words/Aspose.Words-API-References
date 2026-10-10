---
title: "Aspose::Words::Saving::ImageSavingArgs class"
linktitle: "ImageSavingArgs"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::ImageSavingArgs Klasse. Stellt Daten für das ImageSaving()-Ereignis bereit. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class


Stellt Daten für das [ImageSaving()](../iimagesavingcallback/imagesaving/) Ereignis bereit. Weitere Informationen finden Sie im [Dokument speichern](https://docs.aspose.com/words/cpp/save-a-document/) Dokumentationsartikel.

```cpp
class ImageSavingArgs : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_CurrentShape](./get_currentshape/)() const | Liefert das [ShapeBase](../../aspose.words.drawing/shapebase/) Objekt, das der Form oder Gruppenform entspricht, die gespeichert werden soll. |
| [get_Document](./get_document/)() | Liefert das Dokumentobjekt, das gerade gespeichert wird. |
| [get_ImageFileName](./get_imagefilename/)() const | Liest oder setzt den Dateinamen (ohne Pfad), in dem das Bild gespeichert wird. |
| [get_ImageStream](./get_imagestream/)() const | Ermöglicht die Angabe des Streams, in dem das Bild gespeichert wird. |
| [get_IsImageAvailable](./get_isimageavailable/)() const | Gibt **true** zurück, wenn das aktuelle Bild für den Export verfügbar ist. |
| [get_KeepImageStreamOpen](./get_keepimagestreamopen/)() const | Gibt an, ob Aspose.Words den Stream nach dem Speichern eines Bildes offen lassen oder schließen soll. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Setter für [Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName](./get_imagefilename/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Setter für [Aspose::Words::Saving::ImageSavingArgs::get_ImageStream](./get_imagestream/). |
| [set_ImageStream](./set_imagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepImageStreamOpen](./set_keepimagestreamopen/)(bool) | Setter für [Aspose::Words::Saving::ImageSavingArgs::get_KeepImageStreamOpen](./get_keepimagestreamopen/). |
| static [Type](./type/)() |  |
## Hinweise


Standardmäßig speichert Aspose.Words ein Dokument als HTML, indem es jedes Bild in einer separaten Datei ablegt. Aspose.Words verwendet den Dokumentdateinamen und eine eindeutige Nummer, um für jedes im Dokument gefundene Bild einen eindeutigen Dateinamen zu erzeugen.

[ImageSavingArgs](./) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

Um Ihre eigene Logik zur Generierung von Bilddateinamen anzuwenden, verwenden Sie die Eigenschaften [ImageFileName](./get_imagefilename/), [CurrentShape](./get_currentshape/) und [IsImageAvailable](./get_isimageavailable/).

Um Bilder in Streams statt in Dateien zu speichern, verwenden Sie die Eigenschaft [ImageStream](./get_imagestream/).
## Siehe auch

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
