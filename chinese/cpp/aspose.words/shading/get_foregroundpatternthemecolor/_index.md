---
title: "Aspose::Words::Shading::get_ForegroundPatternThemeColor 方法"
linktitle: "get_ForegroundPatternThemeColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Shading::get_ForegroundPatternThemeColor 方法。获取或设置与此 Shading 对象关联的已应用配色方案中的前景图案主题颜色（在 C++ 中）。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words/shading/get_foregroundpatternthemecolor/
---
## Shading::get_ForegroundPatternThemeColor method


获取或设置与此 [Shading](../) 对象关联的已应用配色方案中的前景图案主题颜色。

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Shading::get_ForegroundPatternThemeColor()
```


## 示例



展示如何为 shading 纹理设置前景色和背景色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Shading> shading = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::Texture12Pt5Percent);
shading->set_ForegroundPatternThemeColor(Aspose::Words::Themes::ThemeColor::Dark1);
shading->set_BackgroundPatternThemeColor(Aspose::Words::Themes::ThemeColor::Dark2);

shading->set_ForegroundTintAndShade(0.5);
shading->set_BackgroundTintAndShade(-0.2);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Writeln(u"Foreground and background pattern colors for shading texture.");

doc->Save(get_ArtifactsDir() + u"Font.ForegroundAndBackground.docx");
```

## 另见

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
