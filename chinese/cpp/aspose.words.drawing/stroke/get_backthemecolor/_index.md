---
title: "Aspose::Words::Drawing::Stroke::get_BackThemeColor 方法"
linktitle: "get_BackThemeColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Stroke::get_BackThemeColor 方法。获取或设置表示 C++ 中描边背景颜色的 ThemeColor 对象。"
type: docs
weight: 2167
url: /zh/cpp/aspose.words.drawing/stroke/get_backthemecolor/
---
## Stroke::get_BackThemeColor method


获取或设置表示描边背景颜色的 ThemeColor 对象。

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Stroke::get_BackThemeColor()
```


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

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
