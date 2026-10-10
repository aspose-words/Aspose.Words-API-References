---
title: "Aspose::Words::Font::get_Bidi metodo"
linktitle: "get_Bidi"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Font::get_Bidi metodo. Specifica se il contenuto di questo run deve avere caratteristiche da destra a sinistra in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/font/get_bidi/
---
## Font::get_Bidi method


Specifica se il contenuto di questa sequenza deve avere caratteristiche da destra a sinistra.

```cpp
bool Aspose::Words::Font::get_Bidi()
```

## Note


Questa proprietà, quando è attiva, non deve essere usata con testo fortemente da sinistra a destra. Qualsiasi comportamento in tale condizione non è specificato. Questa proprietà, quando è disattiva, non deve essere usata con testo fortemente da destra a sinistra. Qualsiasi comportamento in tale condizione non è specificato.

Quando il contenuto di questo run viene visualizzato, tutti i caratteri devono essere trattati come caratteri di script complessi a fini di formattazione. Ciò significa che [BoldBi](../get_boldbi/), [ItalicBi](../get_italicbi/), [SizeBi](../get_sizebi/) e un nome di carattere corrispondente verranno utilizzati durante il rendering di questo run.

Inoltre, quando il contenuto di questo run viene visualizzato, questa proprietà agisce come sovrascrittura da destra a sinistra per i caratteri classificati come "weak types" e "neutral types".

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
