---
title: "Metodo Aspose::Words::Font::get_Italic"
linktitle: "get_Italic"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_Italic. True se il carattere è formattato in corsivo in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words/font/get_italic/
---
## Font::get_Italic method


Vero se il carattere è formattato in corsivo.

```cpp
bool Aspose::Words::Font::get_Italic()
```


## Esempi



Mostra come scrivere testo in corsivo usando un DocumentBuilder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Italic(true);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Italic.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
