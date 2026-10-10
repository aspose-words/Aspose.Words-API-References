---
title: "Aspose::Words::Font::get_Size metod"
linktitle: "get_Size"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_Size metod. Hämtar eller anger teckenstorleken i punkter i C++."
type: docs
weight: 36000
url: /sv/cpp/aspose.words/font/get_size/
---
## Font::get_Size method


Hämtar eller anger teckensnittsstorleken i punkter.

```cpp
double Aspose::Words::Font::get_Size()
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


Visar hur man formaterar en run av text med dess font‑egenskap.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
