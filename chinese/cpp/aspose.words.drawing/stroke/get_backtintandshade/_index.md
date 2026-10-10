---
title: "Aspose::Words::Drawing::Stroke::get_BackTintAndShade method"
linktitle: "get_BackTintAndShade"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Stroke::get_BackTintAndShade method. 获取或设置一个双精度值，以在 C++ 中调亮或调暗描边背景颜色。"
type: docs
weight: 2334
url: /zh/cpp/aspose.words.drawing/stroke/get_backtintandshade/
---
## Stroke::get_BackTintAndShade method


获取或设置用于调亮或调暗描边背景颜色的 double 值。

```cpp
double Aspose::Words::Drawing::Stroke::get_BackTintAndShade()
```

## 备注


此属性允许的值范围为 -1（最暗）到 1（最亮）。零（0）为中性。尝试将此属性设置为小于 -1 或大于 1 的值将导致 [ArgumentOutOfRangeException](../)。

## 示例



展示如何设置背景主题颜色以及色调和明暗。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Stroke gradient outline.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);
stroke->set_BackTintAndShade(0.2);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeBackThemeColors.docx");
```

## 另见

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
