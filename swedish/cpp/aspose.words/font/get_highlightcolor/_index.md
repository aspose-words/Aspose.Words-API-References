---
title: "Aspose::Words::Font::get_HighlightColor metod"
linktitle: "get_HighlightColor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_HighlightColor metod. Hämtar eller anger markeringsfärgen (markeringsfärg) i C++."
type: docs
weight: 17000
url: /sv/cpp/aspose.words/font/get_highlightcolor/
---
## Font::get_HighlightColor method


Hämtar eller anger markeringsfärgen (marker).

```cpp
System::Drawing::Color Aspose::Words::Font::get_HighlightColor()
```


## Exempel



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
