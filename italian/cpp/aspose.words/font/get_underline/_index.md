---
title: "Aspose::Words::Font::get_Underline metodo"
linktitle: "get_Underline"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Font::get_Underline metodo. Ottiene o imposta il tipo di sottolineatura applicata al carattere in C++."
type: docs
weight: 55000
url: /it/cpp/aspose.words/font/get_underline/
---
## Font::get_Underline method


Ottiene o imposta il tipo di sottolineatura applicata al carattere.

```cpp
Aspose::Words::Underline Aspose::Words::Font::get_Underline()
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

* Enum [Underline](../../underline/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
