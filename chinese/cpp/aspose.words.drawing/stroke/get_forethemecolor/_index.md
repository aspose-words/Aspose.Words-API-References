---
title: "Aspose::Words::Drawing::Stroke::get_ForeThemeColor 方法"
linktitle: "get_ForeThemeColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Stroke::get_ForeThemeColor 方法。获取或设置一个 ThemeColor 对象，表示笔画的前景颜色，适用于 C++。"
type: docs
weight: 10334
url: /zh/cpp/aspose.words.drawing/stroke/get_forethemecolor/
---
## Stroke::get_ForeThemeColor method


获取或设置表示描边前景颜色的 ThemeColor 对象。

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_ForeThemeColor()
```


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

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
