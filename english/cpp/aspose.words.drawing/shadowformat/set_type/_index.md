---
title: Aspose::Words::Drawing::ShadowFormat::set_Type method
linktitle: set_Type
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShadowFormat::set_Type method. Sets the specified ShadowType for ShadowFormat in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.drawing/shadowformat/set_type/
---
## ShadowFormat::set_Type method


Sets the specified [ShadowType](../../shadowtype/) for ShadowFormat.

```cpp
void Aspose::Words::Drawing::ShadowFormat::set_Type(Aspose::Words::Drawing::ShadowType value)
```

## Remarks

 Setting a new shadow type will reset Color and Transparency values to their default ones. Therefore, it makes sense to first set the desired shadow type and only then Color and Transparency values. 
## Examples


Shows how to get shadow color.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Shadow color.docx"));
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(ShadowType::ShadowMixed, shadowFormat->get_Type());
```
## See Also

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
