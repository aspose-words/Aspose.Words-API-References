---
title: "Aspose::Words::Drawing::ShapeBase::get_MarkupLanguage méthode"
linktitle: "get_MarkupLanguage"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "méthode Aspose::Words::Drawing::ShapeBase::get_MarkupLanguage. Obtient le MarkupLanguage utilisé pour cet objet graphique en C++."
type: docs
weight: 39000
url: /fr/cpp/aspose.words.drawing/shapebase/get_markuplanguage/
---
## ShapeBase::get_MarkupLanguage method


Obtient le MarkupLanguage utilisé pour cet objet graphique.

```cpp
Aspose::Words::Drawing::ShapeMarkupLanguage Aspose::Words::Drawing::ShapeBase::get_MarkupLanguage() const
```


## Exemples



Montre comment vérifier la taille d'une forme et le langage de balisage.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, shape->get_MarkupLanguage());
ASPOSE_ASSERT_EQ(System::Drawing::SizeF(300.0f, 300.0f), shape->get_SizeInPoints());
```

## Voir aussi

* Enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
