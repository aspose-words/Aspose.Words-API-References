---
title: "Aspose::Words::Drawing::Fill::OneColorGradient 方法"
linktitle: "OneColorGradient"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Fill::OneColorGradient 方法。将指定的填充设置为单色渐变（C++）。"
type: docs
weight: 25000
url: /zh/cpp/aspose.words.drawing/fill/onecolorgradient/
---
## Fill::OneColorGradient(Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) method


将指定填充设置为单色渐变。

```cpp
void Aspose::Words::Drawing::Fill::OneColorGradient(Aspose::Words::Drawing::GradientStyle style, Aspose::Words::Drawing::GradientVariant variant, double degree)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| style | Aspose::Words::Drawing::GradientStyle | 梯度样式 [GradientStyle](../../gradientstyle/) |
| variant | Aspose::Words::Drawing::GradientVariant | 梯度变体 [GradientVariant](../../gradientvariant/) |
| 度数 | double | 梯度的度数。可以是 0.0（暗）到 1.0（亮）之间的值。 |

## 示例



展示如何使用渐变填充形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 对形状应用单色渐变填充，使用渐变填充的前景色。
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2, 0.1);

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::Horizontal, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant2, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(270, shape->get_Fill()->get_GradientAngle());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 对形状应用双色渐变填充。
shape->get_Fill()->TwoColorGradient(Aspose::Words::Drawing::GradientStyle::FromCorner, Aspose::Words::Drawing::GradientVariant::Variant4);
// 更改渐变填充的背景色。
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// 注意对 "GradientAngle" 的更改适用于 "GradientStyle.FromCorner/GradientStyle.FromCenter"。
// 渐变填充不会产生任何效果，它仅适用于线性渐变。
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(System::Drawing::Color::get_Yellow().ToArgb(), shape->get_Fill()->get_BackColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::FromCorner, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant4, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(0, shape->get_Fill()->get_GradientAngle());

// 如果想获取 "GradientStyle"，请使用合规选项通过 DML 定义形状，
// "GradientVariant" 和 "GradientAngle" 属性在文档保存后可用。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```

## 另见

* Enum [GradientStyle](../../gradientstyle/)
* Enum [GradientVariant](../../gradientvariant/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## Fill::OneColorGradient(System::Drawing::Color, Aspose::Words::Drawing::GradientStyle, Aspose::Words::Drawing::GradientVariant, double) method


使用指定颜色将指定填充设置为单色渐变。

```cpp
void Aspose::Words::Drawing::Fill::OneColorGradient(System::Drawing::Color color, Aspose::Words::Drawing::GradientStyle style, Aspose::Words::Drawing::GradientVariant variant, double degree)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| color | System::Drawing::Color | 用于构建梯度的颜色。 |
| style | Aspose::Words::Drawing::GradientStyle | 梯度样式 [GradientStyle](../../gradientstyle/) |
| variant | Aspose::Words::Drawing::GradientVariant | 梯度变体 [GradientVariant](../../gradientvariant/) |
| 度数 | double | 梯度的度数。可以是 0.0（暗）到 1.0（亮）之间的值。 |

## 示例



展示如何使用渐变填充形状。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 对形状应用单色渐变填充，使用渐变填充的前景色。
shape->get_Fill()->OneColorGradient(System::Drawing::Color::get_Red(), Aspose::Words::Drawing::GradientStyle::Horizontal, Aspose::Words::Drawing::GradientVariant::Variant2, 0.1);

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), shape->get_Fill()->get_ForeColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::Horizontal, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant2, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(270, shape->get_Fill()->get_GradientAngle());

shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 80, 80);
// 对形状应用双色渐变填充。
shape->get_Fill()->TwoColorGradient(Aspose::Words::Drawing::GradientStyle::FromCorner, Aspose::Words::Drawing::GradientVariant::Variant4);
// 更改渐变填充的背景色。
shape->get_Fill()->set_BackColor(System::Drawing::Color::get_Yellow());
// 注意对 "GradientAngle" 的更改适用于 "GradientStyle.FromCorner/GradientStyle.FromCenter"。
// 渐变填充不会产生任何效果，它仅适用于线性渐变。
shape->get_Fill()->set_GradientAngle(15);

ASSERT_EQ(System::Drawing::Color::get_Yellow().ToArgb(), shape->get_Fill()->get_BackColor().ToArgb());
ASSERT_EQ(Aspose::Words::Drawing::GradientStyle::FromCorner, shape->get_Fill()->get_GradientStyle());
ASSERT_EQ(Aspose::Words::Drawing::GradientVariant::Variant4, shape->get_Fill()->get_GradientVariant());
ASPOSE_ASSERT_EQ(0, shape->get_Fill()->get_GradientAngle());

// 如果想获取 "GradientStyle"，请使用合规选项通过 DML 定义形状，
// "GradientVariant" 和 "GradientAngle" 属性在文档保存后可用。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Compliance(Aspose::Words::Saving::OoxmlCompliance::Iso29500_2008_Strict);

doc->Save(get_ArtifactsDir() + u"Shape.GradientFill.docx", saveOptions);
```

## 另见

* Enum [GradientStyle](../../gradientstyle/)
* Enum [GradientVariant](../../gradientvariant/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
