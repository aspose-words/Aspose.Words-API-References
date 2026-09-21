---
title: "Aspose::Words::Drawing::ImageData::ToStream metod"
linktitle: "ToStream"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ImageData::ToStream metod. Skapar och returnerar en ström som innehåller bildens byte i C++."
type: docs
weight: 38000
url: /sv/cpp/aspose.words.drawing/imagedata/tostream/
---
## ImageData::ToStream method


Skapar och returnerar en ström som innehåller bildens byte.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Drawing::ImageData::ToStream()
```

## Anmärkningar


Om bildbytena lagras i formen skapas och returneras ett **MemoryStream**-objekt.

Om bilden är länkad och lagrad i en fil öppnas filen och ett **FileStream**-objekt returneras.

Om bilden är länkad och lagrad på en extern URL laddas filen ner och ett **MemoryStream**-objekt returneras.

Är det anroparens ansvar att disponera strömmobjektet.

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
