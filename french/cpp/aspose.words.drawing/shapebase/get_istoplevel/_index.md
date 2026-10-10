---
title: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel méthode"
linktitle: "get_IsTopLevel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_IsTopLevel méthode. Retourne true si cette forme n'est pas un enfant d'une forme groupée en C++."
type: docs
weight: 36000
url: /fr/cpp/aspose.words.drawing/shapebase/get_istoplevel/
---
## ShapeBase::get_IsTopLevel method


Renvoie **true** si cette forme n'est pas un enfant d'une forme de groupe.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsTopLevel()
```


## Exemples



Montre comment déterminer si une forme fait partie d'une forme groupée.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Par défaut, une forme ne fait partie d'aucune forme groupée et possède donc la propriété "IsTopLevel" définie sur "true".
ASSERT_TRUE(shape->get_IsTopLevel());

auto group = System::MakeObject<Aspose::Words::Drawing::GroupShape>(doc);
group->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

// Une fois que nous intégrons une forme dans une forme groupée, la propriété "IsTopLevel" passe à "false".
ASSERT_FALSE(shape->get_IsTopLevel());
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
