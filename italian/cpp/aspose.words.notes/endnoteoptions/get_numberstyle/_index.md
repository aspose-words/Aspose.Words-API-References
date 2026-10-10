---
title: "Aspose::Words::Notes::EndnoteOptions::get_NumberStyle metodo"
linktitle: "get_NumberStyle"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Notes::EndnoteOptions::get_NumberStyle metodo. Specifica il formato numerico per le note finali numerate automaticamente in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.notes/endnoteoptions/get_numberstyle/
---
## EndnoteOptions::get_NumberStyle method


Specifica il formato numerico per le note finali autoincrementate.

```cpp
Aspose::Words::NumberStyle Aspose::Words::Notes::EndnoteOptions::get_NumberStyle() override
```

## Note


Non tutti gli stili numerici sono applicabili a questa proprietà. Per l'elenco degli stili numerici applicabili vedere la finestra di dialogo Inserisci [Footnote](../../footnote/) o Endnote in Microsoft Word. Se si seleziona uno stile numerico non applicabile, Microsoft Word tornerà a un valore predefinito.

## Esempi



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

## Vedi anche

* Enum [NumberStyle](../../../aspose.words/numberstyle/)
* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
