---
title: "Aspose::Words::Font::get_Color metod"
linktitle: "get_Color"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_Color metod. Hämtar eller anger färgen på teckensnittet i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words/font/get_color/
---
## Font::get_Color method


Hämtar eller anger färgen på teckensnittet.

```cpp
System::Drawing::Color Aspose::Words::Font::get_Color()
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

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
