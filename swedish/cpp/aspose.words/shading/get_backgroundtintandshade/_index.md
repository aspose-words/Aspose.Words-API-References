---
title: "Aspose::Words::Shading::get_BackgroundTintAndShade metod"
linktitle: "get_BackgroundTintAndShade"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Shading::get_BackgroundTintAndShade metod. Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar en bakgrundstematisk färg i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words/shading/get_backgroundtintandshade/
---
## Shading::get_BackgroundTintAndShade method


Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar en bakgrundstematisk färg.

```cpp
double Aspose::Words::Shading::get_BackgroundTintAndShade()
```

## Anmärkningar


De tillåtna värdena ligger i intervallet från -1 (den mörkaste) till 1 (den ljusaste) för denna egenskap.

Noll (0) är neutral.

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

* Class [Shading](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
