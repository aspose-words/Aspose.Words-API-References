---
title: "Metodo Aspose::Words::Notes::FootnoteOptions::get_StartNumber"
linktitle: "get_StartNumber"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Notes::FootnoteOptions::get_StartNumber. Specifica il numero o il carattere iniziale per le prime note a piè di pagina numerate automaticamente in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.notes/footnoteoptions/get_startnumber/
---
## FootnoteOptions::get_StartNumber method


Specifica il numero o il carattere iniziale per le prime note a piè di pagina numerate automaticamente.

```cpp
int32_t Aspose::Words::Notes::FootnoteOptions::get_StartNumber() override
```

## Note


Questa proprietà ha effetto solo quando [RestartRule](../get_restartrule/) è impostata su [Continuous](../../footnotenumberingrule/).

## Esempi



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

* Class [FootnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
