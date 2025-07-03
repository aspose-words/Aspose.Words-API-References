---
title: Aspose::Words::Drawing::ShadowFormat::get_Type method
linktitle: get_Type
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShadowFormat::get_Type method. Gets or sets the specified ShadowType for ShadowFormat in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.drawing/shadowformat/get_type/
---
## ShadowFormat::get_Type method


Gets or sets the specified [ShadowType](../../shadowtype/) for [ShadowFormat](../).

```cpp
Aspose::Words::Drawing::ShadowType Aspose::Words::Drawing::ShadowFormat::get_Type()
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

* Enum [ShadowType](../../shadowtype/)
* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
