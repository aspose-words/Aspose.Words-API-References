---
title: "Méthode Aspose::Words::Drawing::ShapeBase::get_Hidden"
linktitle: "get_Hidden"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Drawing::ShapeBase::get_Hidden. Obtient ou définit une valeur booléenne indiquant si la forme est visible en C++."
type: docs
weight: 22750
url: /fr/cpp/aspose.words.drawing/shapebase/get_hidden/
---
## ShapeBase::get_Hidden method


Obtient ou définit une valeur booléenne indiquant si la forme est visible.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_Hidden()
```


## Exemples



Montre comment masquer la forme.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
if (!shape->get_Hidden())
{
    shape->set_Hidden(true);
}

doc->Save(get_ArtifactsDir() + u"Shape.Hidden.docx");
```

## Voir aussi

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
