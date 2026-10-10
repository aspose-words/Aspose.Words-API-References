---
title: "Aspose::Words::Drawing::ShadowFormat::get_Type 方法"
linktitle: "get_Type"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShadowFormat::get_Type 方法。获取或设置 ShadowFormat 在 C++ 中的指定 ShadowType。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.drawing/shadowformat/get_type/
---
## ShadowFormat::get_Type method


获取或设置指定的 [ShadowType](../../shadowtype/) 用于 [ShadowFormat](../)。

```cpp
Aspose::Words::Drawing::ShadowType Aspose::Words::Drawing::ShadowFormat::get_Type()
```


## 示例



展示如何获取阴影颜色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shadow color.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> shadowFormat = shape->get_ShadowFormat();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shadowFormat->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::ShadowType::ShadowMixed, shadowFormat->get_Type());
```

## 另见

* Enum [ShadowType](../../shadowtype/)
* Class [ShadowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
