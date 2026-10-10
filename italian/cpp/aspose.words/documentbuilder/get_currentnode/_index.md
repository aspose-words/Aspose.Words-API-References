---
title: "Metodo Aspose::Words::DocumentBuilder::get_CurrentNode"
linktitle: "get_CurrentNode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::get_CurrentNode. Ottiene il nodo attualmente selezionato in questo DocumentBuilder in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words/documentbuilder/get_currentnode/
---
## DocumentBuilder::get_CurrentNode method


Ottiene il nodo attualmente selezionato in questo [DocumentBuilder](../).

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::DocumentBuilder::get_CurrentNode()
```

## Note


[CurrentNode](./) is a cursor of [DocumentBuilder](../) and points to a [Node](../../node/) that is a direct child of a [Paragraph](../../paragraph/). Any insert operations you perform using [DocumentBuilder](../) will insert before the [CurrentNode](./).

Quando il paragrafo corrente è vuoto o il cursore è posizionato appena prima della fine di un paragrafo o di un tag di documento strutturato, [CurrentNode](./) restituisce **null**.

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

## Vedi anche

* Class [Node](../../node/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
