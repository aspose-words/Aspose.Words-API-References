---
title: "Aspose::Words::Drawing::ShapeBase::get_ShadowFormat 方法"
linktitle: "get_ShadowFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::ShapeBase::get_ShadowFormat 方法。获取形状的阴影格式（使用 C++）。"
type: docs
weight: 47000
url: /zh/cpp/aspose.words.drawing/shapebase/get_shadowformat/
---
## ShapeBase::get_ShadowFormat method


获取形状的阴影格式设置。

```cpp
System::SharedPtr<Aspose::Words::Drawing::ShadowFormat> Aspose::Words::Drawing::ShapeBase::get_ShadowFormat()
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

* Class [ShadowFormat](../../shadowformat/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
