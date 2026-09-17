---
title: "Aspose::Words::Drawing::ShapeBase::get_Title méthode"
linktitle: "get_Title"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_Title méthode. Obtient ou définit le titre (légende) de l'objet forme actuel en C++."
type: docs
weight: 51000
url: /fr/cpp/aspose.words.drawing/shapebase/get_title/
---
## ShapeBase::get_Title method


Obtient ou définit le titre (légende) de l'objet forme actuel.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Title()
```

## Remarques


La valeur par défaut est une chaîne vide.

Ne peut pas être **null**, mais peut être une chaîne vide.

## Exemples



Montre comment définir le titre d'une forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Créez une forme, donnez‑lui un titre, puis ajoutez‑la au document.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_Width(200);
shape->set_Height(200);
shape->set_Title(u"My cube");

builder->InsertNode(shape);

// Lorsque nous enregistrons un document contenant une forme qui a un titre,
// Aspose.Words stockera ce titre dans le Alt Text de la forme.
doc->Save(get_ArtifactsDir() + u"Shape.Title.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Title.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::String::Empty, shape->get_Title());
ASSERT_EQ(u"Title: My cube", shape->get_AlternativeText());
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
