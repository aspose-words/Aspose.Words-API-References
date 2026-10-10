---
title: "Aspose::Words::Drawing::ShapeBase::get_IsDecorative méthode"
linktitle: "get_IsDecorative"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsDecorative méthode. Obtient ou définit le drapeau qui indique si la forme est décorative dans le document en C++."
type: docs
weight: 25000
url: /fr/cpp/aspose.words.drawing/shapebase/get_isdecorative/
---
## ShapeBase::get_IsDecorative method


Obtient ou définit le drapeau qui indique si la forme est décorative dans le document.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsDecorative()
```


## Exemples



Montre comment définir que la forme est décorative.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Decorative shapes.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(shape->get_IsDecorative());

// Si "AlternativeText" n'est pas vide, la forme ne peut pas être décorative.
// C'est pourquoi notre valeur a changé en 'false'.
shape->set_AlternativeText(u"Alternative text.");
ASSERT_FALSE(shape->get_IsDecorative());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
// Créez une nouvelle forme en tant que décorative.
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_IsDecorative(true);

doc->Save(get_ArtifactsDir() + u"Shape.IsDecorative.docx");
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
