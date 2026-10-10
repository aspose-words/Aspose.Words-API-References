---
title: "Aspose::Words::Drawing::ShapeBase::get_SizeInPoints طريقة"
linktitle: "get_SizeInPoints"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::get_SizeInPoints طريقة. يحصل على حجم الشكل بالنقاط في C++."
type: docs
weight: 49000
url: /ar/cpp/aspose.words.drawing/shapebase/get_sizeinpoints/
---
## ShapeBase::get_SizeInPoints method


يحصل على حجم الشكل بالنقاط.

```cpp
System::Drawing::SizeF Aspose::Words::Drawing::ShapeBase::get_SizeInPoints()
```


## أمثلة



يظهر كيفية التحقق من حجم الشكل ولغة الترميز.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");

ASSERT_EQ(Aspose::Words::Drawing::ShapeMarkupLanguage::Dml, shape->get_MarkupLanguage());
ASPOSE_ASSERT_EQ(System::Drawing::SizeF(300.0f, 300.0f), shape->get_SizeInPoints());
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
