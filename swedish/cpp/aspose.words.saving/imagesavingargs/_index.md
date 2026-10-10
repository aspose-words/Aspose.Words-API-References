---
title: "Aspose::Words::Saving::ImageSavingArgs class"
linktitle: "ImageSavingArgs"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ImageSavingArgs class. Tillhandahåller data för ImageSaving()-händelsen. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class


Tillhandahåller data för [ImageSaving()](../iimagesavingcallback/imagesaving/) händelsen. För att lära dig mer, besök dokumentationsartikeln [Spara ett dokument](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class ImageSavingArgs : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_CurrentShape](./get_currentshape/)() const | Hämtar [ShapeBase](../../aspose.words.drawing/shapebase/) objektet som motsvarar formen eller gruppformen som ska sparas. |
| [get_Document](./get_document/)() | Hämtar dokumentobjektet som för närvarande sparas. |
| [get_ImageFileName](./get_imagefilename/)() const | Hämtar eller anger filnamnet (utan sökväg) där bilden kommer att sparas till. |
| [get_ImageStream](./get_imagestream/)() const | Tillåter att ange strömmen där bilden ska sparas till. |
| [get_IsImageAvailable](./get_isimageavailable/)() const | Returnerar **true** om den aktuella bilden är tillgänglig för export. |
| [get_KeepImageStreamOpen](./get_keepimagestreamopen/)() const | Anger om Aspose.Words ska hålla strömmen öppen eller stänga den efter att en bild har sparats. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImageFileName](./set_imagefilename/)(const System::String\&) | Sättare för [Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName](./get_imagefilename/). |
| [set_ImageStream](./set_imagestream/)(const System::SharedPtr\<System::IO::Stream\>\&) | Sättare för [Aspose::Words::Saving::ImageSavingArgs::get_ImageStream](./get_imagestream/). |
| [set_ImageStream](./set_imagestream/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_KeepImageStreamOpen](./set_keepimagestreamopen/)(bool) | Sättare för [Aspose::Words::Saving::ImageSavingArgs::get_KeepImageStreamOpen](./get_keepimagestreamopen/). |
| static [Type](./type/)() |  |
## Anmärkningar


Som standard, när Aspose.Words sparar ett dokument till HTML, sparar det varje bild i en separat fil. Aspose.Words använder dokumentfilens namn och ett unikt nummer för att generera unika filnamn för varje bild som finns i dokumentet.

[ImageSavingArgs](./) allows to redefine how image file names are generated or to completely circumvent saving of images into files by providing your own stream objects.

För att tillämpa din egen logik för att generera bildfilnamn, använd egenskaperna [ImageFileName](./get_imagefilename/), [CurrentShape](./get_currentshape/) och [IsImageAvailable](./get_isimageavailable/).

För att spara bilder i strömmar istället för filer, använd egenskapen [ImageStream](./get_imagestream/).
## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
