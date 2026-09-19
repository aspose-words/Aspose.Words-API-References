---
title: "Aspose::Words::Font::get_Outline metodo"
linktitle: "get_Outline"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Font::get_Outline metodo. Vero se il carattere è formattato come contorno in C++."
type: docs
weight: 31000
url: /it/cpp/aspose.words/font/get_outline/
---
## Font::get_Outline method


True se il font è formattato come contorno.

```cpp
bool Aspose::Words::Font::get_Outline()
```


## Esempi



Mostra come creare un blocco di testo formattato come contorno.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Imposta il flag Outline per cambiare il colore di riempimento del testo a bianco e
// lasciare un sottile contorno attorno a ogni carattere nel colore originale del testo.
builder->get_Font()->set_Outline(true);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has an outline.");

doc->Save(get_ArtifactsDir() + u"Font.Outline.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
