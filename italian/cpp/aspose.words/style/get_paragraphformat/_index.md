---
title: "Aspose::Words::Style::get_ParagraphFormat metodo"
linktitle: "get_ParagraphFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Style::get_ParagraphFormat metodo. Restituisce la formattazione del paragrafo dello stile in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words/style/get_paragraphformat/
---
## Style::get_ParagraphFormat method


Ottiene la formattazione del paragrafo dello stile.

```cpp
System::SharedPtr<Aspose::Words::ParagraphFormat> Aspose::Words::Style::get_ParagraphFormat()
```

## Note


Per gli stili di carattere e di elenco questa proprietà restituisce **null**.

## Esempi



Mostra come creare e utilizzare uno stile di paragrafo con formattazione elenco.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea uno stile di paragrafo personalizzato.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Crea un elenco e assicurati che i paragrafi che usano questo stile lo utilizzino.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Applica lo stile di paragrafo al paragrafo corrente del document builder, quindi aggiungi del testo.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Modifica lo stile del DocumentBuilder in uno che non abbia formattazione di elenco e scrivi un altro paragrafo.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## Vedi anche

* Class [ParagraphFormat](../../paragraphformat/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
