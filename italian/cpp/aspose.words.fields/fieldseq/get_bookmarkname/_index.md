---
title: "Aspose::Words::Fields::FieldSeq::get_BookmarkName metodo"
linktitle: "get_BookmarkName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldSeq::get_BookmarkName metodo. Ottiene o imposta un nome di segnalibro che si riferisce a un elemento altrove nel documento anziché nella posizione corrente in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fields/fieldseq/get_bookmarkname/
---
## FieldSeq::get_BookmarkName method


Ottiene o imposta il nome del segnalibro che si riferisce a un elemento altrove nel documento anziché nella posizione corrente.

```cpp
System::String Aspose::Words::Fields::FieldSeq::get_BookmarkName()
```


## Esempi



Mostra come combinare l'indice e i campi di sequenza.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un campo TOC può creare una voce nel suo indice per ogni campo SEQ trovato nel documento.
// Ogni voce contiene il paragrafo che contiene il campo SEQ,
// e il numero della pagina su cui appare il campo.
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

// Configura questo campo TOC per avere una proprietà SequenceIdentifier con valore "MySequence".
fieldToc->set_TableOfFiguresLabel(u"MySequence");

// Configura questo campo TOC per rilevare solo i campi SEQ che si trovano entro i limiti di un segnalibro
// denominato "TOCBookmark".
fieldToc->set_BookmarkName(u"TOCBookmark");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

ASSERT_EQ(u" TOC  \\c MySequence \\b TOCBookmark", fieldToc->GetFieldCode());

// I campi SEQ mostrano un conteggio che incrementa ad ogni campo SEQ.
// Questi campi mantengono anche conteggi separati per ogni sequenza nominata univoca
// identificato dalla proprietà "SequenceIdentifier" del campo SEQ.
// Inserisci un campo SEQ che ha un identificatore di sequenza che corrisponde a quello del TOC
// proprietà TableOfFiguresLabel. Questo campo non creerà una voce nell'indice poiché è al di fuori
// dei limiti del segnalibro designati da "BookmarkName".
builder->Write(u"MySequence #");
auto fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will not show up in the TOC because it is outside of the bookmark.");

builder->StartBookmark(u"TOCBookmark");

// La sequenza di questo campo SEQ corrisponde alla proprietà "TableOfFiguresLabel" del TOC ed è entro i limiti del segnalibro.
// Il paragrafo che contiene questo campo apparirà nell'indice come voce.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", will show up in the TOC next to the entry for the above caption.");

// La sequenza di questo campo SEQ non corrisponde alla proprietà "TableOfFiguresLabel" del TOC,
// ed è entro i limiti del segnalibro. Il suo paragrafo non apparirà nell'indice come voce.
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"OtherSequence");
builder->Writeln(u", will not show up in the TOC because it's from a different sequence identifier.");

// La sequenza di questo campo SEQ corrisponde alla proprietà "TableOfFiguresLabel" del TOC ed è entro i limiti del segnalibro.
// Questo campo fa anche riferimento a un altro segnalibro. Il contenuto di quel segnalibro apparirà nella voce dell'indice per questo campo SEQ.
// Il campo SEQ stesso non visualizzerà il contenuto di quel segnalibro.
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
fieldSeq->set_BookmarkName(u"SEQBookmark");
ASSERT_EQ(u" SEQ  MySequence SEQBookmark", fieldSeq->GetFieldCode());

// Crea un segnalibro con contenuti che appariranno nella voce dell'indice a causa del campo SEQ sopra che lo fa riferimento.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(u"SEQBookmark");
builder->Write(u"MySequence #");
fieldSeq = System::ExplicitCast<Aspose::Words::Fields::FieldSeq>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSequence, true));
fieldSeq->set_SequenceIdentifier(u"MySequence");
builder->Writeln(u", text from inside SEQBookmark.");
builder->EndBookmark(u"SEQBookmark");

builder->EndBookmark(u"TOCBookmark");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SEQ.Bookmark.docx");
```

## Vedi anche

* Class [FieldSeq](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
