---
title: "Aspose::Words::Font::get_Name metodo"
linktitle: "get_Name"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Font::get_Name metodo. Ottiene o imposta il nome del carattere in C++."
type: docs
weight: 25000
url: /it/cpp/aspose.words/font/get_name/
---
## Font::get_Name method


Ottiene o imposta il nome del carattere.

```cpp
System::String Aspose::Words::Font::get_Name()
```

## Note


Durante il recupero, restituisce [NameAscii](../get_nameascii/).

Durante l'impostazione, assegna [NameAscii](../get_nameascii/), [NameBi](../get_namebi/), [NameFarEast](../get_namefareast/) e [NameOther](../get_nameother/) al valore specificato.

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


Mostra come formattare un run di testo usando la sua proprietà font.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```

## Vedi anche

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
