---
title: "Aspose::Words::Shading::get_BackgroundPatternThemeColor metod"
linktitle: "get_BackgroundPatternThemeColor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Shading::get_BackgroundPatternThemeColor metod. Hämtar eller anger bakgrundsmönstrets temafärg i det tillämpade färgschemat som är associerat med detta Shading-objekt i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/shading/get_backgroundpatternthemecolor/
---
## Shading::get_BackgroundPatternThemeColor method


Hämtar eller anger bakgrundsmönstrets temafärg i det tillämpade färgschemat som är associerat med detta [Shading](../) objekt.

```cpp
Aspose::Words::Themes::ThemeColor Aspose::Words::Shading::get_BackgroundPatternThemeColor()
```


## Exempel



Visar hur man ställer in förgrunds- och bakgrundsfärger för skuggningstextur.
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

## Se även

* Enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
