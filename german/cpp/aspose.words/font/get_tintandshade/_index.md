---
title: "Aspose::Words::Font::get_TintAndShade Methode"
linktitle: "get_TintAndShade"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_TintAndShade Methode. Gibt einen double-Wert zurück oder legt ihn fest, der eine Farbe aufhellt oder abdunkelt in C++."
type: docs
weight: 54000
url: /de/cpp/aspose.words/font/get_tintandshade/
---
## Font::get_TintAndShade method


Liest oder setzt einen Double-Wert, der eine Farbe aufhellt oder abdunkelt.

```cpp
double Aspose::Words::Font::get_TintAndShade()
```

## Hinweise


Die zulässigen Werte liegen für diese Eigenschaft im Bereich von -1 (am dunkelsten) bis 1 (am hellsten).

Null (0) ist neutral.

## Beispiele



Zeigt, wie man einen thematisierten Stil erstellt und verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Erstelle einen Stil mit Themen-Schriftarteigenschaften.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Major);
style->get_Font()->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
