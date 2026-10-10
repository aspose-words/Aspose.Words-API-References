---
title: "Aspose::Words::Drawing::ImageData::get_ImageBytes method"
linktitle: "get_ImageBytes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ImageData::get_ImageBytes method. Obtient ou définit les octets bruts de l'image stockée dans la forme en C++."
type: docs
weight: 13000
url: /fr/cpp/aspose.words.drawing/imagedata/get_imagebytes/
---
## ImageData::get_ImageBytes method


Obtient ou définit les octets bruts de l'image stockée dans la forme.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::get_ImageBytes()
```

## Remarques


Définir la valeur à **null** ou un tableau vide supprimera l'image de la forme.

Retourne **null** si l'image n'est pas stockée dans le document (par ex. l'image est probablement liée dans ce cas).

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
