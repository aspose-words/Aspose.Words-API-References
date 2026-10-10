---
title: "Metodo Aspose::Words::Font::ClearFormatting"
linktitle: "ClearFormatting"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::ClearFormatting. Ripristina la formattazione predefinita del carattere in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/font/clearformatting/
---
## Font::ClearFormatting method


Ripristina la formattazione predefinita del carattere.

```cpp
void Aspose::Words::Font::ClearFormatting()
```

## Note


Rimuove tutta la formattazione del carattere specificata esplicitamente sull'oggetto da cui è stato ottenuto [Font](../) in modo che la formattazione del carattere venga ereditata dal genitore appropriato.

## Esempi



Mostra come inserire un campo collegamento ipertestuale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Inserisci un collegamento ipertestuale e enfatizzalo con una formattazione personalizzata.
// Il collegamento ipertestuale sarà un pezzo di testo cliccabile che ci porterà alla posizione specificata nell'URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Ctrl + clic sinistro sul collegamento nel testo in Microsoft Word ci porterà all'URL tramite una nuova finestra del browser web.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
