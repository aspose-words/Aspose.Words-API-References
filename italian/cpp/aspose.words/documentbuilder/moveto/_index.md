---
title: "Metodo Aspose::Words::DocumentBuilder::MoveTo"
linktitle: "MoveTo"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::MoveTo. Sposta il cursore su un nodo inline o alla fine di un paragrafo in C++."
type: docs
weight: 51000
url: /it/cpp/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder::MoveTo method


Sposta il cursore su un nodo inline o alla fine di un paragrafo.

```cpp
void Aspose::Words::DocumentBuilder::MoveTo(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nodo | const System::SharedPtr\<Aspose::Words::Node\>\& | Il nodo deve essere un paragrafo o un figlio diretto di un paragrafo. |
## Note


Quando *node* è un nodo a livello inline, il cursore viene spostato su questo nodo e il contenuto successivo verrà inserito prima di quel nodo.

Quando *node* è un [Paragraph](../../paragraph/), il cursore viene spostato alla fine del paragrafo e il contenuto successivo verrà inserito subito prima dell'interruzione del paragrafo.

Quando *node* è un nodo a livello di blocco ma non un [Paragraph](../../paragraph/), il cursore viene spostato alla fine del primo paragrafo all'interno del nodo a livello di blocco e il contenuto successivo verrà inserito subito prima dell'interruzione del paragrafo.

## Esempi



Mostra come spostare il cursore di un DocumentBuilder verso nodi diversi in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un segnalibro valido, un'entità che consiste di nodi racchiusi da un nodo di inizio segnalibro,
// e un nodo di fine segnalibro.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Bookmark contents.");
builder->EndBookmark(u"MyBookmark");

System::SharedPtr<Aspose::Words::NodeCollection> firstParagraphNodes = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, firstParagraphNodes->idx_get(0)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Run, firstParagraphNodes->idx_get(1)->get_NodeType());
ASSERT_EQ(u"Bookmark contents.", firstParagraphNodes->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::NodeType::BookmarkEnd, firstParagraphNodes->idx_get(2)->get_NodeType());

// Il cursore del DocumentBuilder è sempre davanti al nodo che abbiamo aggiunto per ultimo.
// Se il cursore del builder si trova alla fine del documento, il suo nodo corrente sarà null.
// Il nodo precedente è il nodo di fine segnalibro che abbiamo aggiunto per ultimo.
// Aggiungere nuovi nodi con il builder li aggiungerà al nodo finale.
ASSERT_TRUE(System::TestTools::IsNull(builder->get_CurrentNode()));

// Se desideriamo modificare una parte diversa del documento con il builder,
// dovremo spostare il suo cursore sul nodo che desideriamo modificare.
builder->MoveToBookmark(u"MyBookmark");

// Spostandolo su un segnalibro lo si sposterà al primo nodo compreso tra i nodi di inizio e fine del segnalibro, l'esecuzione racchiusa.
ASPOSE_ASSERT_EQ(firstParagraphNodes->idx_get(1), builder->get_CurrentNode());

// Possiamo anche spostare il cursore su un nodo individuale in questo modo.
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->GetChildNodes(Aspose::Words::NodeType::Any, false)->idx_get(0));

ASSERT_EQ(Aspose::Words::NodeType::BookmarkStart, builder->get_CurrentNode()->get_NodeType());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), builder->get_CurrentParagraph());
ASSERT_TRUE(builder->get_IsAtStartOfParagraph());

// Possiamo utilizzare metodi specifici per spostarci all'inizio/fine di un documento.
builder->MoveToDocumentEnd();

ASSERT_TRUE(builder->get_IsAtEndOfParagraph());

builder->MoveToDocumentStart();

ASSERT_TRUE(builder->get_IsAtStartOfParagraph());
```


Mostra come spostare la posizione del cursore di un [DocumentBuilder](../) a un nodo specificato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Run 1. ");

// Il document builder ha un cursore, che funge da parte del documento
// dove il builder aggiunge nuovi nodi quando utilizziamo i suoi metodi di costruzione del documento.
// Questo cursore funziona allo stesso modo del cursore lampeggiante di Microsoft Word,
// e inoltre finisce sempre immediatamente dopo qualsiasi nodo che il builder ha appena inserito.
// Per aggiungere contenuto a una parte diversa del documento,
// possiamo spostare il cursore a un nodo diverso con il metodo "MoveTo".
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

// Il cursore è ora davanti al nodo a cui lo abbiamo spostato.
// Aggiungere una seconda run lo inserirà davanti alla prima run.
builder->Writeln(u"Run 2. ");

ASSERT_EQ(u"Run 2. \rRun 1.", doc->GetText().Trim());

// Sposta il cursore alla fine del documento per continuare ad aggiungere testo alla fine come prima.
builder->MoveTo(doc->get_LastSection()->get_Body()->get_LastParagraph());
builder->Writeln(u"Run 3. ");

ASSERT_EQ(u"Run 2. \rRun 1. \rRun 3.", doc->GetText().Trim());
```

## Vedi anche

* Class [Node](../../node/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
