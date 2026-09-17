---
title: "Aspose::Words::Drawing::ImageData::SetImage méthode"
linktitle: "SetImage"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ImageData::SetImage méthode. Définit l'image que la forme affiche en C++."
type: docs
weight: 35000
url: /fr/cpp/aspose.words.drawing/imagedata/setimage/
---
## ImageData::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Définit l'image affichée par la forme.

```cpp
void Aspose::Words::Drawing::ImageData::SetImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | L'objet image. |

## Voir aussi

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## ImageData::SetImage(const System::SharedPtr\<System::IO::Stream\>\&) method


Définit l'image affichée par la forme.

```cpp
void Aspose::Words::Drawing::ImageData::SetImage(const System::SharedPtr<System::IO::Stream> &stream)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| flux | const System::SharedPtr\<System::IO::Stream\>\& | Le flux qui contient l'image. |

## Voir aussi

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## ImageData::SetImage(const System::String\&) method


Définit l'image affichée par la forme.

```cpp
void Aspose::Words::Drawing::ImageData::SetImage(const System::String &fileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Le fichier image. Peut être un nom de fichier ou une URL. |

## Exemples



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

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## ImageData::SetImage(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Drawing::ImageData::SetImage(std::basic_istream<CharType, Traits> &stream)
```

## Voir aussi

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
