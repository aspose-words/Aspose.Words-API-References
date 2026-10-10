---
title: "Aspose::Words::Drawing::Stroke::get_JoinStyle 方法"
linktitle: "get_JoinStyle"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Stroke::get_JoinStyle 方法。定义了在 C++ 中折线的连接样式。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.drawing/stroke/get_joinstyle/
---
## Stroke::get_JoinStyle method


定义折线的连接样式。

```cpp
Aspose::Words::Drawing::JoinStyle Aspose::Words::Drawing::Stroke::get_JoinStyle()
```

## 备注


默认值是 [Round](../../joinstyle/)。

## 示例



展示如何更改笔画属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);

// 基本形状，例如矩形，具有两个可见部分。
// 1 -  填充，适用于形状轮廓内的区域：
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_White());

// 2 -  标记形状轮廓的笔画：
// 修改此形状笔画的各种属性。
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_On(true);
stroke->set_Weight(5);
stroke->set_Color(System::Drawing::Color::get_Red());
stroke->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDashDotDot);
stroke->set_JoinStyle(Aspose::Words::Drawing::JoinStyle::Miter);
stroke->set_EndCap(Aspose::Words::Drawing::EndCap::Square);
stroke->set_LineStyle(Aspose::Words::Drawing::ShapeLineStyle::Triple);
stroke->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Red(), System::Drawing::Color::get_Blue(), Aspose::Words::Drawing::GradientStyle::Vertical, Aspose::Words::Drawing::GradientVariant::Variant1);

doc->Save(get_ArtifactsDir() + u"Shape.Stroke.docx");
```

## 另见

* Enum [JoinStyle](../../joinstyle/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
