---
title: "Aspose::Words::Drawing::ShapeBase::get_SizeInPoints méthode"
linktitle: "get_SizeInPoints"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Drawing::ShapeBase::get_SizeInPoints méthode. Obtient la taille de la forme en points en C++."
type: docs
weight: 49000
url: /fr/cpp/aspose.words.drawing/shapebase/get_sizeinpoints/
---
## ShapeBase::get_SizeInPoints method


Obtient la taille de la forme en points.

```cpp
System::Drawing::SizeF Aspose::Words::Drawing::ShapeBase::get_SizeInPoints()
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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
