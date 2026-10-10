---
title: "Metodo Aspose::Words::Style::get_ListFormat"
linktitle: "get_ListFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Style::get_ListFormat. Fornisce l'accesso alle proprietà di formattazione dell'elenco di uno stile di paragrafo in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words/style/get_listformat/
---
## Style::get_ListFormat method


Fornisce l'accesso alle proprietà di formattazione dell'elenco di uno stile di paragrafo.

```cpp
System::SharedPtr<Aspose::Words::Lists::ListFormat> Aspose::Words::Style::get_ListFormat()
```

## Note


Questa proprietà è valida solo per gli stili di paragrafo. Per altri tipi di stile questa proprietà restituisce **null**.

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

* Class [ListFormat](../../../aspose.words.lists/listformat/)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
