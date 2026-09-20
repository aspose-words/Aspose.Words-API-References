---
title: "Aspose::Words::Drawing::GlowFormat 类"
linktitle: "GlowFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::GlowFormat 类。表示对象在 C++ 中的发光格式化。"
type: docs
weight: 1500
url: /zh/cpp/aspose.words.drawing/glowformat/
---
## GlowFormat class


表示对象的发光格式。

```cpp
class GlowFormat : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Color](./get_color/)() | 获取或设置一个 **Color** 对象，表示发光效果的颜色。默认值是 **Black**。 |
| [get_Radius](./get_radius/)() | 获取或设置一个 double 值，表示发光效果半径的长度（单位为点 (pt)）。默认值为 0.0。 |
| [get_Transparency](./get_transparency/)() | 获取或设置发光效果的透明度程度，取值范围为 0.0（不透明）到 1.0（透明）。默认值为 0.0。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | 从父对象中移除 [GlowFormat](./)。 |
| [set_Color](./set_color/)(System::Drawing::Color) | 用于 [Aspose::Words::Drawing::GlowFormat::get_Color](./get_color/) 的 setter。 |
| [set_Radius](./set_radius/)(double) | 用于 [Aspose::Words::Drawing::GlowFormat::get_Radius](./get_radius/) 的 setter。 |
| [set_Transparency](./set_transparency/)(double) | 用于 [Aspose::Words::Drawing::GlowFormat::get_Transparency](./get_transparency/) 的 setter。 |
| static [Type](./type/)() |  |
## 备注


使用 [Glow](../shapebase/get_glow/) 属性来访问对象的发光属性。您不应直接创建 [GlowFormat](./) 类的实例。

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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
