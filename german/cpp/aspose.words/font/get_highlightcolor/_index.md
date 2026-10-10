---
title: "Aspose::Words::Font::get_HighlightColor Methode"
linktitle: "get_HighlightColor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_HighlightColor Methode. Liest oder setzt die Hervorhebungs‑ (Markierungs‑)Farbe in C++."
type: docs
weight: 17000
url: /de/cpp/aspose.words/font/get_highlightcolor/
---
## Font::get_HighlightColor method


Liest oder setzt die Hervorhebungs‑ (Marker‑)Farbe.

```cpp
System::Drawing::Color Aspose::Words::Font::get_HighlightColor()
```


## Beispiele



Zeigt, wie man einen Text‑Run mit seiner Schriftarteigenschaft formatiert.
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

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
