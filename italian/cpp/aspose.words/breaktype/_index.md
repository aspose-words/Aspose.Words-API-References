---
title: "Enum Aspose::Words::BreakType"
linktitle: "BreakType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BreakType enum. Specifica il tipo di interruzione all'interno di un documento in C++."
type: docs
weight: 82000
url: /it/cpp/aspose.words/breaktype/
---
## BreakType enum


Specifica il tipo di interruzione all'interno di un documento.

```cpp
enum class BreakType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| ParagraphBreak | 0 | Interruzione tra paragrafi. |
| PageBreak | 1 | Interruzione di pagina esplicita. |
| ColumnBreak | 2 | Interruzione di colonna esplicita. |
| SectionBreakContinuous | 3 | Specifica l'inizio di una nuova sezione nella stessa pagina della sezione precedente. |
| SectionBreakNewColumn | 4 | Specifica l'inizio di una nuova sezione nella nuova colonna. |
| SectionBreakNewPage | 5 | Specifica l'inizio di una nuova sezione in una nuova pagina. |
| SectionBreakEvenPage | 6 | Specifica l'inizio di una nuova sezione in una nuova pagina pari. |
| SectionBreakOddPage | 7 | Specifica l'inizio di una nuova sezione in una pagina dispari. |
| LineBreak | 8 | Interruzione di riga esplicita. |


## Esempi



Mostra come inserire un indice (TOC) in un documento utilizzando gli stili di intestazione come voci.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un indice per la prima pagina del documento.
// Configura l'indice per includere i paragrafi con intestazioni di livello da 1 a 3.
// Inoltre, imposta le sue voci come collegamenti ipertestuali che ci porteranno
// alla posizione dell'intestazione quando si fa clic con il tasto sinistro in Microsoft Word.
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Popola l'indice aggiungendo paragrafi con stili di intestazione.
// Ogni intestazione di questo tipo con un livello compreso tra 1 e 3 creerà una voce nella tabella.
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// Un indice è un campo di un tipo che deve essere aggiornato per mostrare un risultato aggiornato.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```


Mostra come applicare e ripristinare le impostazioni di configurazione della pagina alle sezioni di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Modifica le proprietà di configurazione della pagina per la sezione corrente del builder e aggiungi testo.
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// Se avviamo una nuova sezione utilizzando un document builder,
// eredità le proprietà di configurazione della pagina correnti del builder.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// Possiamo ripristinare le sue proprietà di configurazione della pagina ai valori predefiniti usando il metodo "ClearFormatting".
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
