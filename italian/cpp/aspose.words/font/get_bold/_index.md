---
title: "Aspose::Words::Font::get_Bold metodo"
linktitle: "get_Bold"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Font::get_Bold metodo. Vero se il carattere è formattato in grassetto in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/font/get_bold/
---
## Font::get_Bold method


Vero se il carattere è formattato in grassetto.

```cpp
bool Aspose::Words::Font::get_Bold()
```


## Esempi



Mostra come inserire testo formattato usando [DocumentBuilder](../../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Specifica la formattazione del carattere, poi aggiungi il testo.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
