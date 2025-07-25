---
title: Aspose::Words::Drawing::ShadowFormat::get_Color method
linktitle: get_Color
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShadowFormat::get_Color method. Gets a Color object that represents the color for the shadow. The default value is Black in C++.'
type: docs
weight: 2500
url: /cpp/aspose.words.drawing/shadowformat/get_color/
---
## ShadowFormat::get_Color method


Gets a **Color** object that represents the color for the shadow. The default value is **Black**.

```cpp
System::Drawing::Color Aspose::Words::Drawing::ShadowFormat::get_Color()
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

* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
