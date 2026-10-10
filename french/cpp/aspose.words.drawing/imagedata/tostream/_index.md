---
title: "Aspose::Words::Drawing::ImageData::ToStream method"
linktitle: "ToStream"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ImageData::ToStream method. Crée et renvoie un flux contenant les octets de l'image en C++."
type: docs
weight: 38000
url: /fr/cpp/aspose.words.drawing/imagedata/tostream/
---
## ImageData::ToStream method


Crée et renvoie un flux contenant les octets de l'image.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Drawing::ImageData::ToStream()
```

## Remarques


Si les octets de l'image sont stockés dans la forme, crée et renvoie un objet **MemoryStream**.

Si l'image est liée et stockée dans un fichier, ouvre le fichier et renvoie un objet **FileStream**.

Si l'image est liée et stockée à une URL externe, télécharge le fichier et renvoie un objet **MemoryStream**.

Est-ce la responsabilité de l'appelant de libérer l'objet flux.

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
