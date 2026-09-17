---
title: "Aspose::Words::Story::get_StoryType méthode"
linktitle: "get_StoryType"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Story::get_StoryType. Obtient le type de cette histoire en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words/story/get_storytype/
---
## Story::get_StoryType method


Obtient le type de cette histoire.

```cpp
Aspose::Words::StoryType Aspose::Words::Story::get_StoryType() override
```


## Exemples



Montre comment supprimer toutes les formes d'un nœud.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Utilisez un DocumentBuilder pour insérer une forme. Il s'agit d'une forme en ligne,
// qui a un paragraphe parent, qui est un nœud enfant du Body de la première section.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Nous pouvons supprimer toutes les formes des paragraphes enfants de ce Corps.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Voir aussi

* Enum [StoryType](../../storytype/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
