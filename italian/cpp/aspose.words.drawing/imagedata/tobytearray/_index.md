---
title: "Aspose::Words::Drawing::ImageData::ToByteArray metodo"
linktitle: "ToByteArray"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ImageData::ToByteArray metodo. Restituisce i byte dell'immagine per qualsiasi immagine indipendentemente dal fatto che l'immagine sia memorizzata o collegata in C++."
type: docs
weight: 36000
url: /it/cpp/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData::ToByteArray method


Restituisce i byte dell'immagine per qualsiasi immagine, indipendentemente dal fatto che l'immagine sia memorizzata o collegata.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::ToByteArray()
```

## Note


Se l'immagine è collegata, scarica l'immagine ogni volta che viene chiamata.

## Esempi



Mostra come creare un file immagine dai dati grezzi dell'immagine di una forma.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imgShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_TRUE(imgShape->get_HasImage());

// ToByteArray() restituisce l'array memorizzato nella proprietà ImageBytes.
ASPOSE_ASSERT_EQ(imgShape->get_ImageData()->get_ImageBytes(), imgShape->get_ImageData()->ToByteArray());

// Salva i dati immagine della forma in un file immagine nel file system locale.
{
    System::SharedPtr<System::IO::Stream> imgStream = imgShape->get_ImageData()->ToStream();
    {
        auto outStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Drawing.GetDataFromImage.png", System::IO::FileMode::Create, System::IO::FileAccess::ReadWrite);
        imgStream->CopyTo(outStream);
    }
}
```

## Vedi anche

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
