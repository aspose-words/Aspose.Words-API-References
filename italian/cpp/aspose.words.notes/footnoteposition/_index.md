---
title: "Aspose::Words::Notes::FootnotePosition enum"
linktitle: "FootnotePosition"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Notes::FootnotePosition enum. Definisce la posizione della nota a piè di pagina in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.notes/footnoteposition/
---
## FootnotePosition enum


Definisce la posizione della nota a piè di pagina.

```cpp
enum class FootnotePosition
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| BottomOfPage | 1 | Le note a piè di pagina vengono visualizzate nella parte inferiore di ogni pagina. |
| BeneathText | 2 | Le note a piè di pagina vengono visualizzate sotto il testo in ogni pagina. |


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

## Vedi anche

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
