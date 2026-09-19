---
title: "Aspose::Words::Font::get_ItalicBi metodo"
linktitle: "get_ItalicBi"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Font::get_ItalicBi metodo. Vero se il testo da destra a sinistra è formattato in corsivo in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words/font/get_italicbi/
---
## Font::get_ItalicBi method


Vero se il testo da destra a sinistra è formattato in corsivo.

```cpp
bool Aspose::Words::Font::get_ItalicBi()
```


## Esempi



Mostra come definire set separati di impostazioni del carattere per testo da destra a sinistra e testo da destra a sinistra.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Definisci un set di impostazioni del carattere per testo da sinistra a destra.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Italic(false);
builder->get_Font()->set_Bold(false);
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// Definisci un altro set di impostazioni del carattere per testo da destra a sinistra.
builder->get_Font()->set_NameBi(u"Andalus");
builder->get_Font()->set_SizeBi(24);
builder->get_Font()->set_ItalicBi(true);
builder->get_Font()->set_BoldBi(true);
builder->get_Font()->set_LocaleIdBi(System::MakeObject<System::Globalization::CultureInfo>(u"ar-AR", false)->get_LCID());

// Possiamo anche usare il flag Bidi per indicare se il testo che stiamo per aggiungere
// con il document builder è da destra a sinistra. Quando aggiungiamo testo con questo flag impostato su true,
// verrà formattato usando il set di impostazioni del carattere da destra a sinistra.
builder->get_Font()->set_Bidi(true);
builder->Write(u"مرحبًا");

// Imposta il flag su false e poi aggiungi testo da sinistra a destra.
// Il document builder formatterà questi usando il set di impostazioni del carattere da sinistra a destra.
builder->get_Font()->set_Bidi(false);
builder->Write(u" Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Bidi.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
