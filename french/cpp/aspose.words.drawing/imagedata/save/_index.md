---
title: "Aspose::Words::Drawing::ImageData::Save méthode"
linktitle: "Save"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ImageData::Save méthode. Enregistre l'image dans le flux spécifié en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words.drawing/imagedata/save/
---
## ImageData::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Enregistre l'image dans le flux spécifié.

```cpp
void Aspose::Words::Drawing::ImageData::Save(const System::SharedPtr<System::IO::Stream> &stream)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Le flux où enregistrer l'image. |
## Remarques


Est-ce la responsabilité de l'appelant de libérer l'objet flux.

## Voir aussi

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## ImageData::Save(const System::String\&) method


Enregistre l'image dans un fichier.

```cpp
void Aspose::Words::Drawing::ImageData::Save(const System::String &fileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Le nom de fichier où enregistrer l'image. |

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

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## ImageData::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Drawing::ImageData::Save(std::basic_ostream<CharType, Traits> &stream)
```

## Voir aussi

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
