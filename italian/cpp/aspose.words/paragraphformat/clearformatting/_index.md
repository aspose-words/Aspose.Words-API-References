---
title: "Aspose::Words::ParagraphFormat::ClearFormatting metodo"
linktitle: "ClearFormatting"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ParagraphFormat::ClearFormatting metodo. Ripristina la formattazione predefinita del paragrafo in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/paragraphformat/clearformatting/
---
## ParagraphFormat::ClearFormatting method


Ripristina la formattazione del paragrafo predefinita.

```cpp
void Aspose::Words::ParagraphFormat::ClearFormatting()
```


## Esempi



Mostra come annidare un elenco all'interno di un altro elenco.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un elenco ci permette di organizzare e decorare insiemi di paragrafi con simboli prefisso e rientri.
// Possiamo creare elenchi nidificati aumentando il livello di rientro.
// Possiamo avviare e terminare un elenco usando la proprietà "ListFormat" di un document builder.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Crea un elenco outline per le intestazioni.
System::SharedPtr<Aspose::Words::Lists::List> outlineList = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::OutlineNumbers);
builder->get_ListFormat()->set_List(outlineList);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"This is my Chapter 1");

// Crea un elenco numerato.
System::SharedPtr<Aspose::Words::Lists::List> numberedList = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);
builder->get_ListFormat()->set_List(numberedList);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Normal);
builder->Writeln(u"Numbered list item 1.");

// Ogni paragrafo che contiene un elenco avrà questo flag.
ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsListItem());
ASSERT_TRUE(builder->get_ParagraphFormat()->get_IsListItem());

// Crea un elenco puntato.
System::SharedPtr<Aspose::Words::Lists::List> bulletedList = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault);
builder->get_ListFormat()->set_List(bulletedList);
builder->get_ParagraphFormat()->set_LeftIndent(72);
builder->Writeln(u"Bulleted list item 1.");
builder->Writeln(u"Bulleted list item 2.");
builder->get_ParagraphFormat()->ClearFormatting();

// Ripristina l'elenco numerato.
builder->get_ListFormat()->set_List(numberedList);
builder->Writeln(u"Numbered list item 2.");
builder->Writeln(u"Numbered list item 3.");

// Ripristina l'elenco outline.
builder->get_ListFormat()->set_List(outlineList);
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"This is my Chapter 2");

builder->get_ParagraphFormat()->ClearFormatting();

builder->get_Document()->Save(get_ArtifactsDir() + u"Lists.NestedLists.docx");
```

## Vedi anche

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
