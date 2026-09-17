---
title: "Aspose::Words::Drawing::ImageData::get_ImageType méthode"
linktitle: "get_ImageType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ImageData::get_ImageType méthode. Obtient le type de l'image en C++."
type: docs
weight: 15000
url: /fr/cpp/aspose.words.drawing/imagedata/get_imagetype/
---
## ImageData::get_ImageType method


Obtient le type de l'image.

```cpp
Aspose::Words::Drawing::ImageType Aspose::Words::Drawing::ImageData::get_ImageType()
```


## Exemples



Montre comment extraire des images d'un document et les enregistrer sur le système de fichiers local en tant que fichiers individuels.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Obtenez la collection de formes du document,
// et enregistrez les données d'image de chaque forme contenant une image sous forme de fichier sur le système de fichiers local.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> s)>>([](System::SharedPtr<Aspose::Words::Node> s) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Drawing::Shape>(s))->get_HasImage();
}))));

int32_t imageIndex = 0;
for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        // Les données d'image des formes peuvent contenir des images dans de nombreux formats d'image possibles.
        // Nous pouvons déterminer automatiquement une extension de fichier pour chaque image, en fonction de son format.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```

## Voir aussi

* Enum [ImageType](../../imagetype/)
* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
