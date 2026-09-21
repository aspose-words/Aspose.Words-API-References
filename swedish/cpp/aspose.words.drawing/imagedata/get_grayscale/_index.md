---
title: "Aspose::Words::Drawing::ImageData::get_GrayScale‑metod"
linktitle: "get_GrayScale"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ImageData::get_GrayScale‑metod. Bestämmer om en bild ska visas i gråskala i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words.drawing/imagedata/get_grayscale/
---
## ImageData::get_GrayScale method


Bestämmer om en bild kommer att visas i gråskaläge.

```cpp
bool Aspose::Words::Drawing::ImageData::get_GrayScale()
```

## Anmärkningar


Standardvärdet är **false**.

## Exempel



Visar hur man redigerar en figurs bilddata.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");
auto sourceShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));

auto dstDoc = System::MakeObject<Aspose::Words::Document>();

// Importera en figur från källdokumentet och lägg till den i det första stycket.
auto importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

// Den importerade figuren innehåller en bild. Vi kan komma åt bildens egenskaper och rådata via ImageData‑objektet.
System::SharedPtr<Aspose::Words::Drawing::ImageData> imageData = importedShape->get_ImageData();
imageData->set_Title(u"Imported Image");

ASSERT_TRUE(imageData->get_HasImage());

// Om en bild saknar kanter kommer dess ImageData‑objekt att definiera kantfärgen som tom.
ASSERT_EQ(4, imageData->get_Borders()->get_Count());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, imageData->get_Borders()->idx_get(0)->get_Color());

// Denna bild länkar inte till någon annan figur eller bildfil i det lokala filsystemet.
ASSERT_FALSE(imageData->get_IsLink());
ASSERT_FALSE(imageData->get_IsLinkOnly());

// Egenskaperna "Brightness" och "Contrast" definierar bildens ljusstyrka och kontrast
// på en skala från 0 till 1, med standardvärdet 0,5.
imageData->set_Brightness(0.8);
imageData->set_Contrast(1.0);

// Ovanstående ljusstyrke- och kontrastvärden har skapat en bild med mycket vitt.
// Vi kan välja en färg med ChromaKey‑egenskapen för att ersätta den med transparens, till exempel vitt.
imageData->set_ChromaKey(System::Drawing::Color::get_White());

// Importera källfiguren igen och sätt bilden till monokrom.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_GrayScale(true);

// Importera källfiguren igen för att skapa en tredje bild och sätt den till BiLevel.
// BiLevel sätter varje pixel till antingen svart eller vitt, beroende på vilket som är närmast den ursprungliga färgen.
importedShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(dstDoc->ImportNode(sourceShape, true));
dstDoc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(importedShape);

importedShape->get_ImageData()->set_BiLevel(true);

// Beskärning bestäms på en skala från 0 till 1. Beskärning av en sida med 0,3
// kommer att ta bort 30 % av bilden på den beskärda sidan.
importedShape->get_ImageData()->set_CropBottom(0.3);
importedShape->get_ImageData()->set_CropLeft(0.3);
importedShape->get_ImageData()->set_CropTop(0.3);
importedShape->get_ImageData()->set_CropRight(0.3);

dstDoc->Save(get_ArtifactsDir() + u"Drawing.ImageData.docx");
```

## Se även

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
