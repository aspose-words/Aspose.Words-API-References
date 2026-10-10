---
title: "Aspose::Words::Drawing::ImageData-klass"
linktitle: "ImageData"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ImageData-klass. Definierar en bild för en form. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.drawing/imagedata/
---
## ImageData class


Definierar en bild för en form. För att lära dig mer, besök dokumentationsartikeln [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/).

```cpp
class ImageData : public Aspose::Words::IBorderAttrSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [FitImageToShape](./fitimagetoshape/)() | Anpassar bilddata till [Shape](../shape/) ram så att bilddataens bildförhållande matchar bildförhållandet för [Shape](../shape/) ram. |
| [get_BiLevel](./get_bilevel/)() | Bestämmer om en bild kommer att visas i svartvitt. |
| [get_Borders](./get_borders/)() | Hämtar samlingen av bildens kanter. Kanter har endast effekt för infogade bilder. |
| [get_Brightness](./get_brightness/)() | Hämtar eller anger bildens ljusstyrka. Värdet för denna egenskap måste vara ett tal mellan 0.0 (mörkast) till 1.0 (ljusast). |
| [get_ChromaKey](./get_chromakey/)() | Definierar färgvärdet för bilden som kommer att behandlas som transparent. |
| [get_Contrast](./get_contrast/)() | Hämtar eller anger kontrasten för den angivna bilden. Värdet för denna egenskap måste vara ett tal mellan 0.0 (minsta kontrast) till 1.0 (största kontrast). |
| [get_CropBottom](./get_cropbottom/)() | Definierar andelen av bildens borttagning från den nedre sidan. |
| [get_CropLeft](./get_cropleft/)() | Definierar andelen av bildens borttagning från den vänstra sidan. |
| [get_CropRight](./get_cropright/)() | Definierar andelen av bildens borttagning från den högra sidan. |
| [get_CropTop](./get_croptop/)() | Definierar andelen av bildens borttagning från den övre sidan. |
| [get_GrayScale](./get_grayscale/)() | Bestämmer om en bild kommer att visas i gråskaläge. |
| [get_HasImage](./get_hasimage/)() | Returnerar **true** om formen har bildbytes eller länkar till en bild. |
| [get_ImageBytes](./get_imagebytes/)() | Hämtar eller anger de råa byte för bilden som lagras i formen. |
| [get_ImageSize](./get_imagesize/)() | Hämtar information om bildens storlek och upplösning. |
| [get_ImageType](./get_imagetype/)() | Hämtar bildens typ. |
| [get_IsLink](./get_islink/)() | Returnerar **true** om bilden är länkad till formen (när [SourceFullName](./get_sourcefullname/) är angivet). |
| [get_IsLinkOnly](./get_islinkonly/)() | Returnerar **true** om bilden är länkad och inte lagrad i dokumentet. |
| [get_SourceFullName](./get_sourcefullname/)() | Hämtar eller anger sökvägen och namnet på källfilen för den länkade bilden. |
| [get_Title](./get_title/)() | Definierar titeln på en bild. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Sparar bilden i den angivna strömmen. |
| [Save](./save/)(const System::String\&) | Sparar bilden i en fil. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_BiLevel](./set_bilevel/)(bool) | Sättare för [Aspose::Words::Drawing::ImageData::get_BiLevel](./get_bilevel/). |
| [set_Brightness](./set_brightness/)(double) | Sättare för [Aspose::Words::Drawing::ImageData::get_Brightness](./get_brightness/). |
| [set_ChromaKey](./set_chromakey/)(System::Drawing::Color) | Sättare för [Aspose::Words::Drawing::ImageData::get_ChromaKey](./get_chromakey/). |
| [set_Contrast](./set_contrast/)(double) | Sättare för [Aspose::Words::Drawing::ImageData::get_Contrast](./get_contrast/). |
| [set_CropBottom](./set_cropbottom/)(double) | Sättare för [Aspose::Words::Drawing::ImageData::get_CropBottom](./get_cropbottom/). |
| [set_CropLeft](./set_cropleft/)(double) | Sättare för [Aspose::Words::Drawing::ImageData::get_CropLeft](./get_cropleft/). |
| [set_CropRight](./set_cropright/)(double) | Sättare för [Aspose::Words::Drawing::ImageData::get_CropRight](./get_cropright/). |
| [set_CropTop](./set_croptop/)(double) | Sättare för [Aspose::Words::Drawing::ImageData::get_CropTop](./get_croptop/). |
| [set_GrayScale](./set_grayscale/)(bool) | Sättare för [Aspose::Words::Drawing::ImageData::get_GrayScale](./get_grayscale/). |
| [set_ImageBytes](./set_imagebytes/)(const System::ArrayPtr\<uint8_t\>\&) | Sättare för [Aspose::Words::Drawing::ImageData::get_ImageBytes](./get_imagebytes/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::ImageData::get_SourceFullName](./get_sourcefullname/). |
| [set_Title](./set_title/)(const System::String\&) | Sättare för [Aspose::Words::Drawing::ImageData::get_Title](./get_title/). |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Anger bilden som formen visar. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Anger bilden som formen visar. |
| [SetImage](./setimage/)(const System::String\&) | Anger bilden som formen visar. |
| [SetImage](./setimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [ToByteArray](./tobytearray/)() | Returnerar bildens byte för vilken bild som helst, oavsett om den är lagrad eller länkad. |
| [ToImage](./toimage/)() | Hämtar bilden som är lagrad i formen som ett **Image**-objekt. |
| [ToStream](./tostream/)() | Skapar och returnerar en ström som innehåller bildens byte. |
| static [Type](./type/)() |  |
## Anmärkningar


Använd egenskapen [ImageData](../shape/get_imagedata/) för att komma åt och ändra bilden i en form. Du skapar inte instanser av klassen [ImageData](./) direkt.

En bild kan lagras i en form, länkas till en extern fil eller både och (länkad och lagrad i dokumentet).

Oavsett om bilden är lagrad i formen eller länkad kan du alltid komma åt den faktiska bilden med metoderna [ToByteArray](./tobytearray/), [ToStream](./tostream/), [ToImage](./toimage/) eller [Save()](../). Om bilden är lagrad i formen kan du även direkt komma åt den via egenskapen [ImageBytes](./get_imagebytes/).

För att lagra en bild i en form använder du metoden [SetImage()](../). För att länka en bild till en form, ange egenskapen [SourceFullName](./get_sourcefullname/).

## Exempel



Visar hur man extraherar bilder från ett dokument och sparar dem till det lokala filsystemet som enskilda filer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Hämta samlingen av former från dokumentet,
// och spara bilddata för varje form med en bild som en fil till det lokala filsystemet.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> s)>>([](System::SharedPtr<Aspose::Words::Node> s) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Drawing::Shape>(s))->get_HasImage();
}))));

int32_t imageIndex = 0;
for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        // Bilddata för former kan innehålla bilder i många möjliga bildformat.
        // Vi kan automatiskt bestämma en filändelse för varje bild baserat på dess format.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```


Visar hur man infogar en länkad bild i ett dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFileName = get_ImageDir() + u"Windows MetaFile.wmf";

// Nedan följer två sätt att applicera en bild på en form så att den kan visas.
// 1 -  Ställ in formen så att den innehåller bilden.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->SetImage(imageFileName);

builder->InsertNode(shape);

doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx");

// Varje bild som vi lagrar i en form kommer att öka storleken på vårt dokument.
ASSERT_TRUE(70000 < System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx")->get_Length());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->RemoveAllChildren();

// 2 -  Ställ in formen så att den länkar till en bildfil i det lokala filsystemet.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->set_SourceFullName(imageFileName);

builder->InsertNode(shape);
doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx");

// Att länka till bilder sparar utrymme och resulterar i ett mindre dokument.
// Dock kan dokumentet bara visa bilden korrekt medan
// bildfilen finns på den plats som formens "SourceFullName"-egenskap pekar på.
ASSERT_TRUE(10000 > System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx")->get_Length());
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
