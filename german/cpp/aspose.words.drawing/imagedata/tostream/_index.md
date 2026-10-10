---
title: "Aspose::Words::Drawing::ImageData::ToStream Methode"
linktitle: "ToStream"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ImageData::ToStream Methode. Erstellt und gibt einen Stream zurück, der die Bildbytes in C++ enthält."
type: docs
weight: 38000
url: /de/cpp/aspose.words.drawing/imagedata/tostream/
---
## ImageData::ToStream method


Erstellt und gibt einen Stream zurück, der die Bildbytes enthält.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Drawing::ImageData::ToStream()
```

## Hinweise


Wenn die Bildbytes in der Form gespeichert sind, wird ein **MemoryStream**‑Objekt erstellt und zurückgegeben.

Wenn das Bild verknüpft und in einer Datei gespeichert ist, wird die Datei geöffnet und ein **FileStream**‑Objekt zurückgegeben.

Wenn das Bild verknüpft und in einer externen URL gespeichert ist, wird die Datei heruntergeladen und ein **MemoryStream**‑Objekt zurückgegeben.

Liegt es in der Verantwortung des Aufrufers, das Stream-Objekt zu entsorgen.

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
