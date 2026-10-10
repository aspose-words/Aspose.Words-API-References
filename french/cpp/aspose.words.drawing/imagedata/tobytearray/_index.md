---
title: "Aspose::Words::Drawing::ImageData::ToByteArray method"
linktitle: "ToByteArray"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ImageData::ToByteArray method. Retourne les octets de l'image pour toute image, qu'elle soit stockée ou liée en C++."
type: docs
weight: 36000
url: /fr/cpp/aspose.words.drawing/imagedata/tobytearray/
---
## ImageData::ToByteArray method


Renvoie les octets de l'image pour toute image, qu'elle soit stockée ou liée.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::ToByteArray()
```

## Remarques


Si l'image est liée, elle télécharge l'image à chaque appel.

## Exemples



Montre comment créer un fichier image à partir des données d'image brutes d'une forme.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imgShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_TRUE(imgShape->get_HasImage());

// ToByteArray() renvoie le tableau stocké dans la propriété ImageBytes.
ASPOSE_ASSERT_EQ(imgShape->get_ImageData()->get_ImageBytes(), imgShape->get_ImageData()->ToByteArray());

// Enregistrez les données d'image de la forme dans un fichier image sur le système de fichiers local.
{
    System::SharedPtr<System::IO::Stream> imgStream = imgShape->get_ImageData()->ToStream();
    {
        auto outStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Drawing.GetDataFromImage.png", System::IO::FileMode::Create, System::IO::FileAccess::ReadWrite);
        imgStream->CopyTo(outStream);
    }
}
```

## Voir aussi

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
