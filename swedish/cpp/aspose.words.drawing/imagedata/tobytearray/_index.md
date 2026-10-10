---
title: "Aspose::Words::Drawing::ImageData::ToByteArray metod"
linktitle: "ToByteArray"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ImageData::ToByteArray metod. Returnerar bildbyte för vilken bild som helst oavsett om bilden är lagrad eller länkad i C++."
type: docs
weight: 36000
url: /sv/cpp/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData::ToByteArray method


Returnerar bildens byte för vilken bild som helst, oavsett om den är lagrad eller länkad.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::ToByteArray()
```

## Anmärkningar


Om bilden är länkad laddas bilden ner varje gång den anropas.

## Exempel



Visar hur man skapar en bildfil från en formes råa bilddata.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imgShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_TRUE(imgShape->get_HasImage());

// ToByteArray() returnerar den array som lagras i egenskapen ImageBytes.
ASPOSE_ASSERT_EQ(imgShape->get_ImageData()->get_ImageBytes(), imgShape->get_ImageData()->ToByteArray());

// Spara formens bilddata till en bildfil i det lokala filsystemet.
{
    System::SharedPtr<System::IO::Stream> imgStream = imgShape->get_ImageData()->ToStream();
    {
        auto outStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Drawing.GetDataFromImage.png", System::IO::FileMode::Create, System::IO::FileAccess::ReadWrite);
        imgStream->CopyTo(outStream);
    }
}
```

## Se även

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
