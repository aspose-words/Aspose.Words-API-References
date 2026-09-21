---
title: "Aspose::Words::Drawing::ImageData::get_ImageBytes metod"
linktitle: "get_ImageBytes"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ImageData::get_ImageBytes metod. Hämtar eller anger de råa bytena för bilden som lagras i formen i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.drawing/imagedata/get_imagebytes/
---
## ImageData::get_ImageBytes method


Hämtar eller anger de råa byte för bilden som lagras i formen.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::get_ImageBytes()
```

## Anmärkningar


Att sätta värdet till **null** eller en tom array kommer att ta bort bilden från formen.

Returnerar **null** om bilden inte är lagrad i dokumentet (t.ex. är bilden sannolikt länkad i detta fall).

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
