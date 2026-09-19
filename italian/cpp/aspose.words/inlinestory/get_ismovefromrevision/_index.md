---
title: "Metodo Aspose::Words::InlineStory::get_IsMoveFromRevision"
linktitle: "get_IsMoveFromRevision"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::InlineStory::get_IsMoveFromRevision. Restituisce true se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il tracciamento delle modifiche era abilitato in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words/inlinestory/get_ismovefromrevision/
---
## InlineStory::get_IsMoveFromRevision method


Restituisce **true** se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il tracciamento delle modifiche era abilitato.

```cpp
bool Aspose::Words::InlineStory::get_IsMoveFromRevision()
```


## Esempi



Mostra come visualizzare le proprietà relative alle revisioni dei nodi [InlineStory](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision footnotes.docx");

// Quando modifichiamo il documento mentre l'opzione \"Track Changes\", trovata in Review -> Tracking,
// è attivata in Microsoft Word, le modifiche che applichiamo contano come revisioni.
// Durante la modifica di un documento usando Aspose.Words, possiamo iniziare a tracciare le revisioni tramite
// invocando il metodo \"StartTrackRevisions\" del documento e interrompendo il tracciamento usando il metodo \"StopTrackRevisions\".
// Possiamo accettare le revisioni per assimilarle nel documento
// oppure rifiutarle per annullare e scartare la modifica proposta.
ASSERT_TRUE(doc->get_HasRevisions());

System::SharedPtr<System::Collections::Generic::List<System::SharedPtr<Aspose::Words::Notes::Footnote>>> footnotes = doc->GetChildNodes(Aspose::Words::NodeType::Footnote, true)->LINQ_Cast<System::SharedPtr<Aspose::Words::Notes::Footnote> >()->LINQ_ToList();

ASSERT_EQ(5, footnotes->get_Count());

// Di seguito sono riportati cinque tipi di revisioni che possono contrassegnare un nodo InlineStory.
// 1 -  Una revisione "insert":
// Questa revisione si verifica quando inseriamo del testo mentre tracciamo le modifiche.
ASSERT_TRUE(footnotes->idx_get(2)->get_IsInsertRevision());

// 2 -  Una revisione "move from":
// Quando evidenziamo del testo in Microsoft Word e lo trasciniamo in una posizione diversa nel documento
// mentre tracciamo le modifiche, compaiono due revisioni.
// La revisione "move from" è una copia del testo originale prima di spostarlo.
ASSERT_TRUE(footnotes->idx_get(4)->get_IsMoveFromRevision());

// 3 -  Una revisione "move to":
// La revisione "move to" è il testo che abbiamo spostato nella sua nuova posizione nel documento.
// "Move from" e "move to" appaiono in coppia per ogni revisione di spostamento che eseguiamo.
// Accettare una revisione di spostamento elimina la revisione "move from" e il suo testo,
// e conserva il testo della revisione "move to".
// Rifiutare una revisione di spostamento, al contrario, conserva la revisione "move from" ed elimina la revisione "move to".
ASSERT_TRUE(footnotes->idx_get(1)->get_IsMoveToRevision());

// 4 -  Una revisione "delete":
// Questa revisione si verifica quando eliminiamo del testo mentre tracciamo le modifiche. Quando eliminiamo il testo in questo modo,
// rimarrà nel documento come revisione finché non accettiamo la revisione,
// che eliminerà definitivamente il testo, o rifiuteremo la revisione, che manterrà il testo eliminato al suo posto.
ASSERT_TRUE(footnotes->idx_get(3)->get_IsDeleteRevision());
```

## Vedi anche

* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
