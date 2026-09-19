---
title: "Metodo Aspose::Words::Document::get_FootnoteOptions"
linktitle: "get_FootnoteOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Document::get_FootnoteOptions. Fornisce opzioni che controllano la numerazione e il posizionamento delle note a piè di pagina in questo documento in C++."
type: docs
weight: 26000
url: /it/cpp/aspose.words/document/get_footnoteoptions/
---
## Document::get_FootnoteOptions method


Fornisce le opzioni che controllano la numerazione e il posizionamento delle note a piè di pagina in questo documento.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteOptions> Aspose::Words::Document::get_FootnoteOptions()
```


## Esempi



Mostra come selezionare un luogo diverso dove il documento raccoglie e visualizza le sue note a piè di pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Una nota a piè di pagina è un modo per allegare un riferimento o un commento a lato al testo
// che non interferisce con il flusso del testo principale.
// L'inserimento di una nota a piè di pagina aggiunge un piccolo simbolo di riferimento in apice
// nel testo principale dove inseriamo la nota a piè di pagina.
// Ogni nota a piè di pagina crea anche una voce in fondo alla pagina, composta da un simbolo
// che corrisponde al simbolo di riferimento nel testo principale.
// Il testo di riferimento che passiamo al metodo "InsertFootnote" del costruttore di documenti.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote contents.");

// Possiamo usare la proprietà "Position" per determinare dove il documento posizionerà tutte le sue note a piè di pagina.
// Se impostiamo il valore della proprietà "Position" su "FootnotePosition.BottomOfPage",
// ogni nota a piè di pagina verrà visualizzata in fondo alla pagina che contiene il suo segno di riferimento. Questo è il valore predefinito.
// Se impostiamo il valore della proprietà "Position" su "FootnotePosition.BeneathText",
// ogni nota a piè di pagina verrà visualizzata alla fine del testo della pagina che contiene il suo segno di riferimento.
doc->get_FootnoteOptions()->set_Position(footnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionFootnote.docx");
```


Mostra come modificare lo stile numerico dei segni di riferimento di note a piè di pagina/note di chiusura.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Le note a piè di pagina e le note di chiusura sono un modo per allegare un riferimento o un commento a lato al testo
// che non interferisce con il flusso del testo principale.
// L'inserimento di una nota a piè di pagina/nota di chiusura aggiunge un piccolo simbolo di riferimento in apice
// nel testo principale dove inseriamo la nota a piè di pagina/nota di chiusura.
// Ogni nota a piè di pagina/nota di chiusura crea anche una voce, che consiste in un simbolo che corrisponde al riferimento
// nel testo principale. Il testo di riferimento che passiamo al metodo "InsertEndnote" del costruttore di documenti.
// Le voci delle note a piè di pagina, per impostazione predefinita, vengono visualizzate in fondo a ogni pagina che contiene
// i loro simboli di riferimento, e le note di chiusura vengono visualizzate alla fine del documento.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.", u"Custom footnote reference mark");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.", u"Custom endnote reference mark");

// Per impostazione predefinita, il simbolo di riferimento per ogni nota a piè di pagina e nota di chiusura è il suo indice
// tra tutte le note a piè di pagina/di chiusura del documento. Ogni documento mantiene conteggi separati
// per le note a piè di pagina e per le note di chiusura. Per impostazione predefinita, le note a piè di pagina mostrano i loro numeri usando numeri arabi,
// e le note di chiusura mostrano i loro numeri in numeri romani minuscoli.
ASSERT_EQ(Aspose::Words::NumberStyle::Arabic, doc->get_FootnoteOptions()->get_NumberStyle());
ASSERT_EQ(Aspose::Words::NumberStyle::LowercaseRoman, doc->get_EndnoteOptions()->get_NumberStyle());

// Possiamo usare la proprietà "NumberStyle" per applicare stili di numerazione personalizzati a note a piè di pagina e note di chiusura.
// Questo non influenzerà le note a piè di pagina/note di chiusura con segni di riferimento personalizzati.
doc->get_FootnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseRoman);
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::UppercaseLetter);

doc->Save(get_ArtifactsDir() + u"InlineStory.RefMarkNumberStyle.docx");
```


Mostra come riavviare la numerazione di note a piè di pagina/note di chiusura in determinati punti del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Le note a piè di pagina e le note di chiusura sono un modo per allegare un riferimento o un commento a lato al testo
// che non interferisce con il flusso del testo principale.
// L'inserimento di una nota a piè di pagina/nota di chiusura aggiunge un piccolo simbolo di riferimento in apice
// nel testo principale dove inseriamo la nota a piè di pagina/nota di chiusura.
// Ogni nota a piè di pagina/nota di chiusura crea anche una voce, che consiste in un simbolo che corrisponde al riferimento
// nel testo principale. Il testo di riferimento che passiamo al metodo "InsertEndnote" del costruttore di documenti.
// Le voci delle note a piè di pagina, per impostazione predefinita, vengono visualizzate in fondo a ogni pagina che contiene
// i loro simboli di riferimento, e le note di chiusura vengono visualizzate alla fine del documento.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 4.");

builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");
builder->Write(u"Text 4. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 4.");

// Per impostazione predefinita, il simbolo di riferimento per ogni nota a piè di pagina e nota di chiusura è il suo indice
// tra tutte le note a piè di pagina/di chiusura del documento. Ogni documento mantiene conteggi separati
// per note a piè di pagina e note di chiusura e non riavvia questi conteggi in nessun momento.
ASSERT_EQ(doc->get_FootnoteOptions()->get_RestartRule(), Aspose::Words::Notes::FootnoteNumberingRule::Default);
ASSERT_EQ(Aspose::Words::Notes::FootnoteNumberingRule::Default, Aspose::Words::Notes::FootnoteNumberingRule::Continuous);

// Possiamo usare la proprietà "RestartRule" per far riavviare il documento
// i conteggi di note a piè di pagina/note di chiusura in una nuova pagina o sezione.
doc->get_FootnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartPage);
doc->get_EndnoteOptions()->set_RestartRule(Aspose::Words::Notes::FootnoteNumberingRule::RestartSection);

doc->Save(get_ArtifactsDir() + u"InlineStory.NumberingRule.docx");
```


Mostra come impostare un numero al quale il documento inizia il conteggio di note a piè di pagina/note di chiusura.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Le note a piè di pagina e le note di chiusura sono un modo per allegare un riferimento o un commento a lato al testo
// che non interferisce con il flusso del testo principale.
// L'inserimento di una nota a piè di pagina/nota di chiusura aggiunge un piccolo simbolo di riferimento in apice
// nel testo principale dove inseriamo la nota a piè di pagina/nota di chiusura.
// Ogni nota a piè di pagina/note di chiusura crea anche una voce, che consiste in un simbolo
// che corrisponde al simbolo di riferimento nel testo principale.
// Il testo di riferimento che passiamo al metodo \"InsertEndnote\" del costruttore del documento.
// Le voci delle note a piè di pagina, per impostazione predefinita, vengono visualizzate in fondo a ogni pagina che contiene
// i loro simboli di riferimento, e le note di chiusura vengono visualizzate alla fine del documento.
builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote 3.");

builder->InsertParagraph();

builder->Write(u"Text 1. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 1.");
builder->Write(u"Text 2. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 2.");
builder->Write(u"Text 3. ");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote 3.");

// Per impostazione predefinita, il simbolo di riferimento per ogni nota a piè di pagina e nota di chiusura è il suo indice
// tra tutte le note a piè di pagina/di chiusura del documento. Ogni documento mantiene conteggi separati
// per note a piè di pagina e per note di chiusura, che entrambe iniziano da 1.
ASSERT_EQ(1, doc->get_FootnoteOptions()->get_StartNumber());
ASSERT_EQ(1, doc->get_EndnoteOptions()->get_StartNumber());

// Possiamo usare la proprietà "StartNumber" per far sì che il documento
// inizii un conteggio di nota a piè di pagina o di nota di chiusura con un numero diverso.
doc->get_EndnoteOptions()->set_NumberStyle(Aspose::Words::NumberStyle::Arabic);
doc->get_EndnoteOptions()->set_StartNumber(50);

doc->Save(get_ArtifactsDir() + u"InlineStory.StartNumber.docx");
```

## Vedi anche

* Class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
