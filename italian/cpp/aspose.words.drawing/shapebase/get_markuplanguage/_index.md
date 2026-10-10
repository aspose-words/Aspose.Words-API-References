---
title: "Aspose::Words::Drawing::ShapeBase::get_MarkupLanguage method"
linktitle: "get_MarkupLanguage"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Drawing::ShapeBase::get_MarkupLanguage. Ottiene MarkupLanguage usato per questo oggetto grafico in C++."
type: docs
weight: 39000
url: /it/cpp/aspose.words.drawing/shapebase/get_markuplanguage/
---
## ShapeBase::get_MarkupLanguage method


Ottiene il MarkupLanguage usato per questo oggetto grafico.

```cpp
Aspose::Words::Drawing::ShapeMarkupLanguage Aspose::Words::Drawing::ShapeBase::get_MarkupLanguage() const
```


## Esempi



Mostra come verificare la dimensione di una forma e il linguaggio di markup.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, shape->get_MarkupLanguage());
ASPOSE_ASSERT_EQ(System::Drawing::SizeF(300.0f, 300.0f), shape->get_SizeInPoints());
```

## Vedi anche

* Enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
