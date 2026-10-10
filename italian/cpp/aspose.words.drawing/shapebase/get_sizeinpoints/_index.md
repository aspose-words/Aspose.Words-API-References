---
title: "Aspose::Words::Drawing::ShapeBase::get_SizeInPoints method"
linktitle: "get_SizeInPoints"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Drawing::ShapeBase::get_SizeInPoints method. Ottiene la dimensione della forma in punti in C++."
type: docs
weight: 49000
url: /it/cpp/aspose.words.drawing/shapebase/get_sizeinpoints/
---
## ShapeBase::get_SizeInPoints method


Ottiene le dimensioni della forma in punti.

```cpp
System::Drawing::SizeF Aspose::Words::Drawing::ShapeBase::get_SizeInPoints()
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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
