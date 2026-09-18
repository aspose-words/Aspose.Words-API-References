---
title: "Aspose::Words::Drawing::ImageData::ToByteArray Methode"
linktitle: "ToByteArray"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ImageData::ToByteArray Methode. Gibt Bildbytes für jedes Bild zurück, unabhängig davon, ob das Bild in C++ gespeichert oder verknüpft ist."
type: docs
weight: 36000
url: /de/cpp/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData::ToByteArray method


Gibt Bildbytes für jedes Bild zurück, unabhängig davon, ob das Bild gespeichert oder verknüpft ist.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::ToByteArray()
```

## Hinweise


Wenn das Bild verknüpft ist, wird das Bild bei jedem Aufruf heruntergeladen.

## Beispiele



Zeigt, wie man aus den Roh‑Bilddaten einer Form eine Bilddatei erstellt.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imgShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_TRUE(imgShape->get_HasImage());

// ToByteArray() gibt das im ImageBytes‑Eigenschaft gespeicherte Array zurück.
ASPOSE_ASSERT_EQ(imgShape->get_ImageData()->get_ImageBytes(), imgShape->get_ImageData()->ToByteArray());

// Speichert die Bilddaten der Form in einer Bilddatei im lokalen Dateisystem.
{
    System::SharedPtr<System::IO::Stream> imgStream = imgShape->get_ImageData()->ToStream();
    {
        auto outStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Drawing.GetDataFromImage.png", System::IO::FileMode::Create, System::IO::FileAccess::ReadWrite);
        imgStream->CopyTo(outStream);
    }
}
```

## Siehe auch

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
