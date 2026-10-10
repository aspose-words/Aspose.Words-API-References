---
title: "Aspose::Words::Font::get_Underline-metod"
linktitle: "get_Underline"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_Underline-metod. Hämtar eller anger typen av understrykning som tillämpas på teckensnittet i C++."
type: docs
weight: 55000
url: /sv/cpp/aspose.words/font/get_underline/
---
## Font::get_Underline method


Hämtar eller anger typen av understrykning som tillämpas på teckensnittet.

```cpp
Aspose::Words::Underline Aspose::Words::Font::get_Underline()
```


## Exempel



Visar hur man infogar formaterad text med hjälp av [DocumentBuilder](../../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ange teckensnittformatering, och lägg sedan till text.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```


Visar hur man infogar ett hyperlänksfält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Infoga en hyperlänk och betona den med anpassad formatering.
// Hyperlänken kommer att vara en klickbar textbit som tar oss till den plats som anges i URL:en.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + vänsterklick på länken i texten i Microsoft Word tar oss till URL:en via ett nytt webbläsarfönster.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```


Visar hur man konfigurerar stil och färg på en textunderstrykning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Aspose::Words::Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(get_ArtifactsDir() + u"Font.Underlines.docx");
```

## Se även

* Enum [Underline](../../underline/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
