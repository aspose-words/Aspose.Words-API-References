---
title: "Aspose::Words::Drawing::ImageData::get_SourceFullName metod"
linktitle: "get_SourceFullName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ImageData::get_SourceFullName metod. Hämtar eller anger sökvägen och namnet på källfilen för den länkade bilden i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words.drawing/imagedata/get_sourcefullname/
---
## ImageData::get_SourceFullName method


Hämtar eller anger sökvägen och namnet på källfilen för den länkade bilden.

```cpp
System::String Aspose::Words::Drawing::ImageData::get_SourceFullName()
```

## Anmärkningar


Standardvärdet är en tom sträng.

Om [SourceFullName](./) inte är en tom sträng, är bilden länkad.

## Exempel



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

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
