---
title: "Aspose::Words::Font::get_TintAndShade-metod"
linktitle: "get_TintAndShade"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_TintAndShade metod. Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar en färg i C++."
type: docs
weight: 54000
url: /sv/cpp/aspose.words/font/get_tintandshade/
---
## Font::get_TintAndShade method


Hämtar eller anger ett dubbelvärde som ljusar upp eller mörkar en färg.

```cpp
double Aspose::Words::Font::get_TintAndShade()
```

## Anmärkningar


De tillåtna värdena ligger i intervallet från -1 (mörkast) till 1 (ljusast) för denna egenskap.

Noll (0) är neutral.

## Exempel



Visar hur man skapar och använder temastil.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Skapa en stil med temafontsegenskaper.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Major);
style->get_Font()->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
