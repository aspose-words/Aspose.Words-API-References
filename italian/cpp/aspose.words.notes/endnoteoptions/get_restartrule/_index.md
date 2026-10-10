---
title: "Aspose::Words::Notes::EndnoteOptions::get_RestartRule metodo"
linktitle: "get_RestartRule"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Notes::EndnoteOptions::get_RestartRule metodo. Determina quando la numerazione automatica riprende in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.notes/endnoteoptions/get_restartrule/
---
## EndnoteOptions::get_RestartRule method


Determina quando il conteggio automatico viene ripristinato.

```cpp
Aspose::Words::Notes::FootnoteNumberingRule Aspose::Words::Notes::EndnoteOptions::get_RestartRule() override
```

## Note


Non tutti i valori sono applicabili alle note finali. Per determinare quali valori sono applicabili, vedere [FootnoteNumberingRule](../../footnotenumberingrule/).

## Esempi



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

## Vedi anche

* Enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
