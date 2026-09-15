---
title: "طريقة Aspose::Words::Shading::get_BackgroundPatternThemeColor"
linktitle: "get_BackgroundPatternThemeColor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Shading::get_BackgroundPatternThemeColor. يحصل على أو يضبط لون نمط الخلفية في مخطط الألوان المطبق المرتبط بهذا الكائن Shading في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words/shading/get_backgroundpatternthemecolor/
---
## Shading::get_BackgroundPatternThemeColor method


يحصل على أو يضبط لون نمط الخلفية في مخطط الألوان المطبق المرتبط بهذا الكائن [Shading](../).

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Shading::get_BackgroundPatternThemeColor()
```


## أمثلة



يظهر كيفية ضبط ألوان المقدمة والخلفية لنسيج التظليل.
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

## انظر أيضًا

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
