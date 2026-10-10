---
title: "Aspose::Words::Drawing::GlowFormat::get_Color 方法"
linktitle: "get_Color"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::GlowFormat::get_Color 方法。获取或设置表示辉光效果颜色的 Color 对象。默认值在 C++ 中为 黑色。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.drawing/glowformat/get_color/
---
## GlowFormat::get_Color method


获取或设置一个 **Color** 对象，表示发光效果的颜色。默认值是 **Black**。

```cpp
System::Drawing::Color Aspose::Words::Drawing::GlowFormat::get_Color()
```


## 示例



展示如何与发光形状效果交互。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Various shapes.docx");
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

shape->get_Glow()->set_Color(System::Drawing::Color::get_Salmon());
shape->get_Glow()->set_Radius(30);
shape->get_Glow()->set_Transparency(0.15);

doc->Save(get_ArtifactsDir() + u"Shape.Glow.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Glow.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::Drawing::Color::FromArgb(217, 250, 128, 114).ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(30, shape->get_Glow()->get_Radius());
ASSERT_NEAR(0.15, shape->get_Glow()->get_Transparency(), 0.01);

shape->get_Glow()->Remove();

ASSERT_EQ(System::Drawing::Color::get_Black().ToArgb(), shape->get_Glow()->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Radius());
ASPOSE_ASSERT_EQ(0, shape->get_Glow()->get_Transparency());
```

## 另见

* Class [GlowFormat](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
