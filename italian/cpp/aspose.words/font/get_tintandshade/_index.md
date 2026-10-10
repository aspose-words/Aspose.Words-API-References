---
title: "Aspose::Words::Font::get_TintAndShade metodo"
linktitle: "get_TintAndShade"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Font::get_TintAndShade metodo. Ottiene o imposta un valore double che schiarisce o scurisce un colore in C++."
type: docs
weight: 54000
url: /it/cpp/aspose.words/font/get_tintandshade/
---
## Font::get_TintAndShade method


Ottiene o imposta un valore double che schiarisce o scurisce un colore.

```cpp
double Aspose::Words::Font::get_TintAndShade()
```

## Note


I valori consentiti sono nell'intervallo da -1 (il più scuro) a 1 (il più chiaro) per questa proprietà.

Zero (0) è neutro.

## Esempi



Mostra come creare e utilizzare uno stile tematico.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Crea uno stile con le proprietà del carattere tematico.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Major);
style->get_Font()->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
