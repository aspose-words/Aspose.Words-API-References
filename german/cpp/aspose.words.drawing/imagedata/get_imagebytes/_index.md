---
title: "Aspose::Words::Drawing::ImageData::get_ImageBytes-Methode"
linktitle: "get_ImageBytes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ImageData::get_ImageBytes-Methode. Ruft die Rohbytes des im Shape gespeicherten Bildes ab oder legt sie fest in C++."
type: docs
weight: 13000
url: /de/cpp/aspose.words.drawing/imagedata/get_imagebytes/
---
## ImageData::get_ImageBytes method


Liest oder legt die Rohbytes des in der shape gespeicherten Bildes fest.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::get_ImageBytes()
```

## Hinweise


Das Setzen des Werts auf **null** oder ein leeres Array entfernt das Bild aus dem Shape.

Gibt **null** zurück, wenn das Bild nicht im Dokument gespeichert ist (z. B. ist das Bild in diesem Fall wahrscheinlich verknüpft).

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
