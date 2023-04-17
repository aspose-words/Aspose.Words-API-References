---
title: Aspose::Words::Drawing::ShapeBase::get_MarkupLanguage method
linktitle: get_MarkupLanguage
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_MarkupLanguage method. Gets MarkupLanguage used for this graphic object in C++.'
type: docs
weight: 39000
url: /cpp/aspose.words.drawing/shapebase/get_markuplanguage/
---
## ShapeBase::get_MarkupLanguage method


Gets MarkupLanguage used for this graphic object.

```cpp
Aspose::Words::Drawing::ShapeMarkupLanguage Aspose::Words::Drawing::ShapeBase::get_MarkupLanguage() const
```


## Examples



Shows how to verify a shape's size and markup language. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

SharedPtr<Shape> shape = builder->InsertImage(ImageDir + u"Transparent background logo.png");

ASSERT_EQ(ShapeMarkupLanguage::Dml, shape->get_MarkupLanguage());
ASPOSE_ASSERT_EQ(System::Drawing::SizeF(300.0f, 300.0f), shape->get_SizeInPoints());
```

## See Also

* Enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
