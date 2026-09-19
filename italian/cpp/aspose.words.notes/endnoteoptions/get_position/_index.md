---
title: "Aspose::Words::Notes::EndnoteOptions::get_Position metodo"
linktitle: "get_Position"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Notes::EndnoteOptions::get_Position metodo. Specifica la posizione delle note finali in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.notes/endnoteoptions/get_position/
---
## EndnoteOptions::get_Position method


Specifica la posizione delle note a pié di pagina.

```cpp
Aspose::Words::Notes::EndnotePosition Aspose::Words::Notes::EndnoteOptions::get_Position()
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
// Ogni nota a piè di pagina crea anche una voce alla fine del documento, composta da un simbolo
// che corrisponde al simbolo di riferimento nel testo principale.
// Il testo di riferimento che passiamo al metodo \"InsertEndnote\" del costruttore del documento.
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote contents.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"This is the second section.");

// Possiamo usare la proprietà \"Position\" per determinare dove il documento posizionerà tutte le sue note a piè di pagina.
// Se impostiamo il valore della proprietà \"Position\" su \"EndnotePosition.EndOfDocument\",
// ogni nota a piè di pagina verrà mostrata in una raccolta alla fine del documento. Questo è il valore predefinito.
// Se impostiamo il valore della proprietà \"Position\" su \"EndnotePosition.EndOfSection\",
// ogni nota a piè di pagina verrà mostrata in una raccolta alla fine della sezione il cui testo contiene il segno di riferimento della nota a piè di pagina.
doc->get_EndnoteOptions()->set_Position(endnotePosition);

doc->Save(get_ArtifactsDir() + u"InlineStory.PositionEndnote.docx");
```

## Vedi anche

* Enum [EndnotePosition](../../endnoteposition/)
* Class [EndnoteOptions](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
