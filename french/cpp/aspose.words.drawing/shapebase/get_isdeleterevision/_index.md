---
title: "Aspose::Words::Drawing::ShapeBase::get_IsDeleteRevision méthode"
linktitle: "get_IsDeleteRevision"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsDeleteRevision méthode. Retourne true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé en C++."
type: docs
weight: 26000
url: /fr/cpp/aspose.words.drawing/shapebase/get_isdeleterevision/
---
## ShapeBase::get_IsDeleteRevision method


Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsDeleteRevision()
```


## Exemples



Montre comment travailler avec les formes de révision.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASSERT_FALSE(doc->get_TrackRevisions());

// Insérez une forme en ligne sans suivre les révisions, ce qui fera que cette forme ne sera pas une révision de quelque nature que ce soit.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Commencez à suivre les révisions puis insérez une autre forme, qui sera une révision.
doc->StartTrackRevisions(u"John Doe");

shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Sun);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->set_Width(100.0);
shape->set_Height(100.0);
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(2, shapes->get_Length());

shapes[0]->Remove();

// Puisque nous avons supprimé cette forme alors que nous suivions les modifications,
// la forme persiste dans le document et compte comme une révision de suppression.
// Accepter cette révision supprimera la forme de façon permanente, et la rejeter la conservera dans le document.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Cube, shapes[0]->get_ShapeType());
ASSERT_TRUE(shapes[0]->get_IsDeleteRevision());

// Et nous avons inséré une autre forme tout en suivant les modifications, ainsi cette forme comptera comme une révision d'insertion.
// Accepter cette révision intégrera cette forme dans le document en tant que non‑révision,
// et rejeter la révision supprimera cette forme de façon permanente.
ASSERT_EQ(Aspose::Words::Drawing::ShapeType::Sun, shapes[1]->get_ShapeType());
ASSERT_TRUE(shapes[1]->get_IsInsertRevision());
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
