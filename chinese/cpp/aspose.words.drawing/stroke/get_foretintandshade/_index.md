---
title: "Aspose::Words::Drawing::Stroke::get_ForeTintAndShade 方法"
linktitle: "get_ForeTintAndShade"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Stroke::get_ForeTintAndShade 方法。获取或设置一个 double 值，用于在 C++ 中调亮或调暗笔画的前景颜色。"
type: docs
weight: 10667
url: /zh/cpp/aspose.words.drawing/stroke/get_foretintandshade/
---
## Stroke::get_ForeTintAndShade method


获取或设置用于调亮或调暗描边前景颜色的 double 值。

```cpp
double Aspose::Words::Drawing::Stroke::get_ForeTintAndShade()
```

## 备注


此属性允许的值范围为 -1（最暗）到 1（最亮）。零（0）为中性。尝试将此属性设置为小于 -1 或大于 1 的值将导致 [ArgumentOutOfRangeException](../)。

## 示例



展示如何设置前景主题颜色以及色调和明暗。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 40);
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
stroke->set_ForeTintAndShade(0.5);

doc->Save(get_ArtifactsDir() + u"Shape.StrokeForeThemeColors.docx");
```

## 另见

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
