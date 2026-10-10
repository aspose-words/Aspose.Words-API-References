---
title: "Aspose::Words::PaperSize enum"
linktitle: "PaperSize"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PaperSize enum. Specifica la dimensione della carta in C++."
type: docs
weight: 109000
url: /it/cpp/aspose.words/papersize/
---
## PaperSize enum


Specifica la dimensione della carta.

```cpp
enum class PaperSize
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| A3 | 0 | 297 x 420 mm. |
| A4 | 1 | 210 x 297 mm. |
| A5 | 2 | 148 x 210 mm. |
| B4 | 3 | 250 x 353 mm. |
| B5 | 4 | 176 x 250 mm. |
| Executive | 5 | 7.25 x 10.5 pollici. |
| Folio | 6 | 8.5 x 13 pollici. |
| Ledger | 7 | 17 x 11 pollici. |
| Legal | 8 | 8.5 x 14 pollici. |
| Letter | 9 | 8.5 x 11 pollici. |
| EnvelopeDL | 10 | 110 x 220 mm. |
| Quarto | 11 | 8.47 x 10.83 inches. |
| Statement | 12 | 8.5 x 5.5 inches. |
| Tabloid | 13 | 11 x 17 inches. |
| Paper10x14 | 14 | 10 x 14 inches. |
| Paper11x17 | 15 | 11 x 17 inches. |
| Number10Envelope | 16 | 4.125 x 9.5 inches. |
| JisB4 | 17 | 257 x 364 mm. |
| JisB5 | 18 | 182 x 257 mm. |
| Personalizzato | 19 | Formato carta personalizzato. |


## Esempi



Mostra come regolare le dimensioni della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```


Mostra come impostare le dimensioni della pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Possiamo modificare le dimensioni della pagina corrente a una dimensione predefinita
// utilizzando la proprietà \"PaperSize\" dell'oggetto PageSetup di questa sezione.
builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Tabloid);

ASPOSE_ASSERT_EQ(792.0, builder->get_PageSetup()->get_PageWidth());
ASPOSE_ASSERT_EQ(1224.0, builder->get_PageSetup()->get_PageHeight());

builder->Writeln(System::String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

// Ogni sezione ha il proprio oggetto PageSetup. Quando utilizziamo un document builder per creare una nuova sezione,
// l'oggetto PageSetup di quella sezione eredita tutti i valori dell'oggetto PageSetup della sezione precedente.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);

ASSERT_EQ(Aspose::Words::PaperSize::Tabloid, builder->get_PageSetup()->get_PaperSize());

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::A5);
builder->Writeln(System::String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

ASPOSE_ASSERT_EQ(419.55, builder->get_PageSetup()->get_PageWidth());
ASPOSE_ASSERT_EQ(595.30, builder->get_PageSetup()->get_PageHeight());

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);

// Imposta una dimensione personalizzata per le pagine di questa sezione.
builder->get_PageSetup()->set_PageWidth(620);
builder->get_PageSetup()->set_PageHeight(480);

ASSERT_EQ(Aspose::Words::PaperSize::Custom, builder->get_PageSetup()->get_PaperSize());

builder->Writeln(System::String::Format(u"This page is {0}x{1}.", builder->get_PageSetup()->get_PageWidth(), builder->get_PageSetup()->get_PageHeight()));

doc->Save(get_ArtifactsDir() + u"PageSetup.PaperSizes.docx");
```


Mostra come costruire manualmente un documento Aspose.Words.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento vuoto contiene una sezione, un corpo e un paragrafo.
// Chiama il metodo "RemoveAllChildren" per rimuovere tutti quei nodi,
// e otterrai un nodo documento senza figli.
doc->RemoveAllChildren();

// Questo documento ora non ha nodi figli compositi a cui possiamo aggiungere contenuti.
// Se desideriamo modificarlo, dovremo ripopolare la sua collezione di nodi.
// Per prima cosa, crea una nuova sezione, quindi aggiungila come figlio al nodo radice del documento.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Imposta alcune proprietà di configurazione della pagina per la sezione.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Una sezione ha bisogno di un corpo, che conterrà e visualizzerà tutti i suoi contenuti
// sulla pagina tra l'intestazione e il piè di pagina della sezione.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Crea un paragrafo, imposta alcune proprietà di formattazione e quindi aggiungilo come figlio al corpo.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Infine, aggiungi del contenuto al documento. Crea un run,
// imposta il suo aspetto e i suoi contenuti, e quindi aggiungilo come figlio al paragrafo.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
