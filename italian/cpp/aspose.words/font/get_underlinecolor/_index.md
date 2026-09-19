---
title: "Metodo Aspose::Words::Font::get_UnderlineColor"
linktitle: "get_UnderlineColor"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_UnderlineColor. Ottiene o imposta il colore della sottolineatura applicata al carattere in C++."
type: docs
weight: 56000
url: /it/cpp/aspose.words/font/get_underlinecolor/
---
## Font::get_UnderlineColor method


Ottiene o imposta il colore della sottolineatura applicata al carattere.

```cpp
System::Drawing::Color Aspose::Words::Font::get_UnderlineColor()
```


## Esempi



Mostra come configurare lo stile e il colore di una sottolineatura di testo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Aspose::Words::Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(get_ArtifactsDir() + u"Font.Underlines.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
