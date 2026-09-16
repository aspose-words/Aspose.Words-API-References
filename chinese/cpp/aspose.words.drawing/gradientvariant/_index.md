---
title: "Aspose::Words::Drawing::GradientVariant enum"
linktitle: "GradientVariant"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::GradientVariant 枚举。指定 C++ 中渐变填充的变体。"
type: docs
weight: 25000
url: /zh/cpp/aspose.words.drawing/gradientvariant/
---
## GradientVariant enum


指定渐变填充的变体。

```cpp
enum class GradientVariant
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 渐变变体 'None'。 |
| Variant1 | 1 | 渐变变体 1。 |
| Variant2 | 2 | 渐变变体 2。 |
| Variant3 | 3 | 渐变变体 3。 |
| Variant4 | 4 | 梯度变体 4。 |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
