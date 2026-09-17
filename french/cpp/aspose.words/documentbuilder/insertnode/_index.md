---
title: "Aspose::Words::DocumentBuilder::InsertNode méthode"
linktitle: "InsertNode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DocumentBuilder::InsertNode méthode. Insère un nœud avant le curseur en C++."
type: docs
weight: 40000
url: /fr/cpp/aspose.words/documentbuilder/insertnode/
---
## DocumentBuilder::InsertNode method


Insère un nœud avant le curseur.

```cpp
void Aspose::Words::DocumentBuilder::InsertNode(const System::SharedPtr<Aspose::Words::Node> &node)
```


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

* Class [Node](../../node/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
