---
title: Aspose::Words::Drawing::ShapeBase::get_ShadowFormat method
linktitle: get_ShadowFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_ShadowFormat method. Gets shadow formatting for the shape in C++.'
type: docs
weight: 47000
url: /cpp/aspose.words.drawing/shapebase/get_shadowformat/
---
## ShapeBase::get_ShadowFormat method


Gets shadow formatting for the shape.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> Aspose::Words::Drawing::ShapeBase::get_ShadowFormat()
```


## Examples



Shows how to get shadow color. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```

## See Also

* Class [ShadowFormat](../../shadowformat/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
