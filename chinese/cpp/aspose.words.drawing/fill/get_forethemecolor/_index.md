---
title: "Aspose::Words::Drawing::Fill::get_ForeThemeColor 方法"
linktitle: "get_ForeThemeColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Drawing::Fill::get_ForeThemeColor 方法。获取或设置一个 ThemeColor 对象，表示填充的前景颜色（在 C++ 中）。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.drawing/fill/get_forethemecolor/
---
## Fill::get_ForeThemeColor method


获取或设置表示填充前景颜色的 ThemeColor 对象。

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Drawing::Fill::get_ForeThemeColor()
```


## 示例



展示如何为前景/背景形状颜色设置主题颜色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::RoundRectangle, 80, 80);

System::SharedPtr<Aspose::Words::Drawing::Fill> fill = shape->get_Fill();
fill->set_ForeThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
fill->set_BackThemeColor(Aspose::Words::Themes::ThemeColor::Background2);

// 注意：不要在字体填充中使用 "BackThemeColor" 和 "BackTintAndShade"。
if (fill->get_BackTintAndShade() == 0)
{
    fill->set_BackTintAndShade(0.2);
}

doc->Save(get_ArtifactsDir() + u"Shape.FillThemeColor.docx");
```

## 另见

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Fill](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
