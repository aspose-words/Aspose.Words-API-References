---
title: "Metodo Aspose::Words::Font::get_LocaleId"
linktitle: "get_LocaleId"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_LocaleId. Ottiene o imposta l'identificatore locale (lingua) dei caratteri formattati in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words/font/get_localeid/
---
## Font::get_LocaleId method


Ottiene o imposta l'identificatore locale (lingua) dei caratteri formattati.

```cpp
int32_t Aspose::Words::Font::get_LocaleId()
```


## Esempi



Mostra come impostare la locale del testo che stiamo aggiungendo con un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Se impostiamo la locale del carattere su Inglese e inseriamo del testo russo,
// il correttore ortografico della locale Inglese non riconoscerà il testo e lo segnalerà come errore ortografico.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());
builder->Writeln(u"Привет!");

// Imposta una locale corrispondente per il testo che stiamo per aggiungere per applicare il correttore ortografico appropriato.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU", false)->get_LCID());
builder->Writeln(u"Привет!");

doc->Save(get_ArtifactsDir() + u"Font.LocaleId.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
