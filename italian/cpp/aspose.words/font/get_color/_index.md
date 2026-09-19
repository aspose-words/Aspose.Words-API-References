---
title: "Metodo Aspose::Words::Font::get_Color"
linktitle: "get_Color"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Font::get_Color. Ottiene o imposta il colore del font in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/font/get_color/
---
## Font::get_Color method


Ottiene o imposta il colore del carattere.

```cpp
System::Drawing::Color Aspose::Words::Font::get_Color()
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

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
