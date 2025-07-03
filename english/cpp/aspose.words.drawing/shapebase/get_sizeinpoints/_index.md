---
title: Aspose::Words::Drawing::ShapeBase::get_SizeInPoints method
linktitle: get_SizeInPoints
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_SizeInPoints method. Gets the size of the shape in points in C++.'
type: docs
weight: 49000
url: /cpp/aspose.words.drawing/shapebase/get_sizeinpoints/
---
## ShapeBase::get_SizeInPoints method


Gets the size of the shape in points.

```cpp
System::Drawing::SizeF Aspose::Words::Drawing::ShapeBase::get_SizeInPoints()
```


## Examples



Shows how to verify a shape's size and markup language. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, shape->get_MarkupLanguage());
ASPOSE_ASSERT_EQ(System::Drawing::SizeF(300.0f, 300.0f), shape->get_SizeInPoints());
```

## See Also

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
