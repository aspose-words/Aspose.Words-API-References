---
title: "Aspose::Words::Paragraph::get_Runs metodo"
linktitle: "get_Runs"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Paragraph::get_Runs metodo. Fornisce l'accesso alla collezione tipizzata di frammenti di testo all'interno del paragrafo in C++."
type: docs
weight: 25000
url: /it/cpp/aspose.words/paragraph/get_runs/
---
## Paragraph::get_Runs method


Fornisce l'accesso alla collezione tipizzata di frammenti di testo all'interno del paragrafo.

```cpp
System::SharedPtr<Aspose::Words::RunCollection> Aspose::Words::Paragraph::get_Runs()
```


## Esempi



Mostra come determinare il tipo di revisione di un nodo inline.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// Quando modifichiamo il documento mentre l'opzione \"Track Changes\", trovata in Review -> Tracking,
// è attivata in Microsoft Word, le modifiche che applichiamo contano come revisioni.
// Durante la modifica di un documento usando Aspose.Words, possiamo iniziare a tracciare le revisioni tramite
// invocando il metodo \"StartTrackRevisions\" del documento e interrompendo il tracciamento usando il metodo \"StopTrackRevisions\".
// Possiamo accettare le revisioni per assimilarle nel documento
// oppure rifiutarle per modificare efficacemente la modifica proposta.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// Il nodo genitore di una revisione è il run a cui la revisione si riferisce. Un Run è un nodo Inline.
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// Di seguito sono riportati cinque tipi di revisioni che possono segnalare un nodo Inline.
// 1 -  Una revisione "insert":
// Questa revisione si verifica quando inseriamo del testo mentre tracciamo le modifiche.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  Una revisione "format":
// Questa revisione si verifica quando modifichiamo la formattazione del testo mentre tracciamo le modifiche.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  Una revisione "move from":
// Quando evidenziamo del testo in Microsoft Word e lo trasciniamo in una posizione diversa nel documento
// mentre tracciamo le modifiche, compaiono due revisioni.
// La revisione "move from" è una copia del testo originale prima di spostarlo.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  Una revisione "move to":
// La revisione "move to" è il testo che abbiamo spostato nella sua nuova posizione nel documento.
// "Move from" e "move to" appaiono in coppia per ogni revisione di spostamento che eseguiamo.
// Accettare una revisione di spostamento elimina la revisione "move from" e il suo testo,
// e conserva il testo della revisione "move to".
// Rifiutare una revisione di spostamento, al contrario, conserva la revisione "move from" ed elimina la revisione "move to".
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  Una revisione "delete":
// Questa revisione si verifica quando eliminiamo del testo mentre tracciamo le modifiche. Quando eliminiamo il testo in questo modo,
// rimarrà nel documento come revisione finché non accettiamo la revisione,
// che eliminerà definitivamente il testo, o rifiuteremo la revisione, che manterrà il testo eliminato al suo posto.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## Vedi anche

* Class [RunCollection](../../runcollection/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
