---
title: "Metodo Aspose::Words::Font::get_HighlightColor"
linktitle: "get_HighlightColor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_HighlightColor. Ottiene o imposta il colore di evidenziazione (marcatore) in C++."
type: docs
weight: 17000
url: /it/cpp/aspose.words/font/get_highlightcolor/
---
## Font::get_HighlightColor method


Ottiene o imposta il colore di evidenziazione (marcatore).

```cpp
System::Drawing::Color Aspose::Words::Font::get_HighlightColor()
```


## Esempi



Mostra come formattare un run di testo usando la sua proprietà font.
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

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
