---
title: "Aspose::Words::Font::get_NameBi metodo"
linktitle: "get_NameBi"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Font::get_NameBi metodo. Restituisce o imposta il nome del carattere in un documento di lingua da destra a sinistra in C++."
type: docs
weight: 27000
url: /it/cpp/aspose.words/font/get_namebi/
---
## Font::get_NameBi method


Restituisce o imposta il nome del carattere in un documento in lingua da destra a sinistra.

```cpp
System::String Aspose::Words::Font::get_NameBi()
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
