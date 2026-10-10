---
title: "Aspose::Words::Drawing::ImageData::ToStream metodo"
linktitle: "ToStream"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ImageData::ToStream metodo. Crea e restituisce uno stream che contiene i byte dell'immagine in C++."
type: docs
weight: 38000
url: /it/cpp/aspose.words.drawing/imagedata/tostream/
---
## ImageData::ToStream method


Crea e restituisce uno stream che contiene i byte dell'immagine.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Drawing::ImageData::ToStream()
```

## Note


Se i byte dell'immagine sono memorizzati nella forma, crea e restituisce un oggetto **MemoryStream**.

Se l'immagine è collegata e memorizzata in un file, apre il file e restituisce un oggetto **FileStream**.

Se l'immagine è collegata e memorizzata in un URL esterno, scarica il file e restituisce un oggetto **MemoryStream**.

È responsabilità del chiamante rilasciare l'oggetto stream.

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
