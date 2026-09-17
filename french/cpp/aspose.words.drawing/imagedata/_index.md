---
title: "Aspose::Words::Drawing::ImageData class"
linktitle: "ImageData"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ImageData class. Définit une image pour une forme. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.drawing/imagedata/
---
## ImageData class


Définit une image pour une forme. Pour en savoir plus, consultez l'article de documentation [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/).

```cpp
class ImageData : public Aspose::Words::IBorderAttrSource
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [FitImageToShape](./fitimagetoshape/)() | Ajuste les données d'image au cadre [Shape](../shape/) afin que le rapport d'aspect des données d'image corresponde au rapport d'aspect du cadre [Shape](../shape/). |
| [get_BiLevel](./get_bilevel/)() | Détermine si une image sera affichée en noir et blanc. |
| [get_Borders](./get_borders/)() | Obtient la collection des bordures de l'image. Les bordures n'ont d'effet que pour les images en ligne. |
| [get_Brightness](./get_brightness/)() | Obtient ou définit la luminosité de l'image. La valeur de cette propriété doit être un nombre compris entre 0.0 (le plus sombre) et 1.0 (le plus lumineux). |
| [get_ChromaKey](./get_chromakey/)() | Définit la valeur de couleur de l'image qui sera traitée comme transparente. |
| [get_Contrast](./get_contrast/)() | Obtient ou définit le contraste de l'image spécifiée. La valeur de cette propriété doit être un nombre compris entre 0.0 (le contraste le plus faible) et 1.0 (le contraste le plus élevé). |
| [get_CropBottom](./get_cropbottom/)() | Définit la fraction de suppression de l'image du côté inférieur. |
| [get_CropLeft](./get_cropleft/)() | Définit la fraction de suppression de l'image du côté gauche. |
| [get_CropRight](./get_cropright/)() | Définit la fraction de suppression de l'image du côté droit. |
| [get_CropTop](./get_croptop/)() | Définit la fraction de suppression de l'image du côté supérieur. |
| [get_GrayScale](./get_grayscale/)() | Détermine si une image sera affichée en mode niveaux de gris. |
| [get_HasImage](./get_hasimage/)() | Renvoie **true** si la forme possède des octets d'image ou lie une image. |
| [get_ImageBytes](./get_imagebytes/)() | Obtient ou définit les octets bruts de l'image stockée dans la forme. |
| [get_ImageSize](./get_imagesize/)() | Obtient les informations sur la taille et la résolution de l'image. |
| [get_ImageType](./get_imagetype/)() | Obtient le type de l'image. |
| [get_IsLink](./get_islink/)() | Renvoie **true** si l'image est liée à la forme (lorsque [SourceFullName](./get_sourcefullname/) est spécifié). |
| [get_IsLinkOnly](./get_islinkonly/)() | Renvoie **true** si l'image est liée et n'est pas stockée dans le document. |
| [get_SourceFullName](./get_sourcefullname/)() | Obtient ou définit le chemin et le nom du fichier source pour l'image liée. |
| [get_Title](./get_title/)() | Définit le titre d'une image. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Enregistre l'image dans le flux spécifié. |
| [Save](./save/)(const System::String\&) | Enregistre l'image dans un fichier. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_BiLevel](./set_bilevel/)(bool) | Définisseur pour [Aspose::Words::Drawing::ImageData::get_BiLevel](./get_bilevel/). |
| [set_Brightness](./set_brightness/)(double) | Définisseur pour [Aspose::Words::Drawing::ImageData::get_Brightness](./get_brightness/). |
| [set_ChromaKey](./set_chromakey/)(System::Drawing::Color) | Définisseur pour [Aspose::Words::Drawing::ImageData::get_ChromaKey](./get_chromakey/). |
| [set_Contrast](./set_contrast/)(double) | Définisseur pour [Aspose::Words::Drawing::ImageData::get_Contrast](./get_contrast/). |
| [set_CropBottom](./set_cropbottom/)(double) | Définisseur pour [Aspose::Words::Drawing::ImageData::get_CropBottom](./get_cropbottom/). |
| [set_CropLeft](./set_cropleft/)(double) | Définisseur pour [Aspose::Words::Drawing::ImageData::get_CropLeft](./get_cropleft/). |
| [set_CropRight](./set_cropright/)(double) | Définisseur pour [Aspose::Words::Drawing::ImageData::get_CropRight](./get_cropright/). |
| [set_CropTop](./set_croptop/)(double) | Définisseur pour [Aspose::Words::Drawing::ImageData::get_CropTop](./get_croptop/). |
| [set_GrayScale](./set_grayscale/)(bool) | Définisseur pour [Aspose::Words::Drawing::ImageData::get_GrayScale](./get_grayscale/). |
| [set_ImageBytes](./set_imagebytes/)(const System::ArrayPtr\<uint8_t\>\&) | Définisseur pour [Aspose::Words::Drawing::ImageData::get_ImageBytes](./get_imagebytes/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::ImageData::get_SourceFullName](./get_sourcefullname/). |
| [set_Title](./set_title/)(const System::String\&) | Définisseur pour [Aspose::Words::Drawing::ImageData::get_Title](./get_title/). |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Définit l'image affichée par la forme. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Définit l'image affichée par la forme. |
| [SetImage](./setimage/)(const System::String\&) | Définit l'image affichée par la forme. |
| [SetImage](./setimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [ToByteArray](./tobytearray/)() | Renvoie les octets de l'image pour toute image, qu'elle soit stockée ou liée. |
| [ToImage](./toimage/)() | Obtient l'image stockée dans la forme en tant qu'objet **Image**. |
| [ToStream](./tostream/)() | Crée et renvoie un flux contenant les octets de l'image. |
| static [Type](./type/)() |  |
## Remarques


Utilisez la propriété [ImageData](../shape/get_imagedata/) pour accéder et modifier l'image à l'intérieur d'une forme. Vous ne créez pas d'instances de la classe [ImageData](./) directement.

Une image peut être stockée à l'intérieur d'une forme, liée à un fichier externe ou les deux (liée et stockée dans le document).

Quel que soit le fait que l'image soit stockée à l'intérieur de la forme ou liée, vous pouvez toujours accéder à l'image réelle en utilisant les méthodes [ToByteArray](./tobytearray/), [ToStream](./tostream/), [ToImage](./toimage/) ou [Save()](../). Si l'image est stockée à l'intérieur de la forme, vous pouvez également y accéder directement via la propriété [ImageBytes](./get_imagebytes/).

Pour stocker une image à l'intérieur d'une forme, utilisez la méthode [SetImage()](../). Pour lier une image à une forme, définissez la propriété [SourceFullName](./get_sourcefullname/).

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


Montre comment insérer une image liée dans un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFileName = get_ImageDir() + u"Windows MetaFile.wmf";

// Voici deux façons d'appliquer une image à une forme afin qu'elle puisse l'afficher.
// 1 -  Définissez la forme pour qu'elle contienne l'image.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->SetImage(imageFileName);

builder->InsertNode(shape);

doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx");

// Chaque image que nous stockons dans une forme augmentera la taille de notre document.
ASSERT_TRUE(70000 < System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx")->get_Length());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->RemoveAllChildren();

// 2 -  Définissez la forme pour qu'elle lie à un fichier image dans le système de fichiers local.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->set_SourceFullName(imageFileName);

builder->InsertNode(shape);
doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx");

// Lier des images permettra d'économiser de l'espace et donnera un document plus petit.
// Cependant, le document ne peut afficher correctement l'image que tant que
// le fichier image est présent à l'emplacement indiqué par la propriété \"SourceFullName\" de la forme.
ASSERT_TRUE(10000 > System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx")->get_Length());
```

## Voir aussi

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
