---
title: "Metodo Aspose::Words::DocumentBuilder::MoveToBookmark"
linktitle: "MoveToBookmark"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBuilder::MoveToBookmark. Sposta il cursore a un segnalibro in C++."
type: docs
weight: 52000
url: /it/cpp/aspose.words/documentbuilder/movetobookmark/
---
## DocumentBuilder::MoveToBookmark(const System::String\&) method


Sposta il cursore su un segnalibro.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | const System::String\& | Il nome del segnalibro verso cui spostare il cursore. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Note


Sposta il cursore in una posizione subito dopo l'inizio del segnalibro con il nome specificato.

Il confronto non è sensibile al maiuscolo/minuscolo. Se il segnalibro non è stato trovato, viene restituito **false** e il cursore non viene spostato.

L'inserimento di nuovo testo non sostituisce il testo esistente del segnalibro.

Nota che alcuni segnalibri nel documento sono assegnati a campi modulo. Spostarsi su un tale segnalibro e inserire testo lì inserisce il testo nel codice del campo modulo. Sebbene ciò non invalidi il campo modulo, il testo inserito non sarà visibile perché diventa parte del codice del campo.

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

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToBookmark(const System::String\&, bool, bool) method


Sposta il cursore su un segnalibro con maggiore precisione.

```cpp
bool Aspose::Words::DocumentBuilder::MoveToBookmark(const System::String &bookmarkName, bool isStart, bool isAfter)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| bookmarkName | const System::String\& | Il nome del segnalibro verso cui spostare il cursore. |
| isStart | bool | Quando **true**, sposta il cursore all'inizio del segnalibro. Quando **false**, sposta il cursore alla fine del segnalibro. |
| isAfter | bool | Quando **true**, sposta il cursore in modo che sia dopo la posizione di inizio o fine del segnalibro. Quando **false**, sposta il cursore in modo che sia prima della posizione di inizio o fine del segnalibro. |

### ReturnValue

**true** if the bookmark was found; **false** otherwise.
## Note


Sposta il cursore in una posizione prima o dopo l'inizio o la fine del segnalibro.

Se la posizione desiderata non è a livello inline, si sposta al paragrafo successivo.

Il confronto non è sensibile al maiuscolo/minuscolo. Se il segnalibro non è stato trovato, viene restituito **false** e il cursore non viene spostato.

## Esempi



Mostra come spostare il cursore del punto di inserimento dei nodi di DocumentBuilder a un segnalibro.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Un segnalibro valido è costituito da un nodo BookmarkStart, un nodo BookmarkEnd con un
// nome di segnalibro corrispondente da qualche parte in seguito, e contenuti racchiusi da quei nodi.
builder->StartBookmark(u"MyBookmark");
builder->Write(u"Hello world! ");
builder->EndBookmark(u"MyBookmark");

// Esistono 4 modi per spostare il cursore di DocumentBuilder a un segnalibro.
// Se ci troviamo tra i nodi BookmarkStart e BookmarkEnd, il cursore sarà all'interno del segnalibro.
// Ciò significa che qualsiasi testo aggiunto dal builder diventerà parte del segnalibro.
// 1 -  Fuori dal segnalibro, davanti al nodo BookmarkStart:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, false));
builder->Write(u"1. ");

ASSERT_EQ(u"Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. Hello world!", doc->GetText().Trim());

// 2 -  All'interno del segnalibro, subito dopo il nodo BookmarkStart:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", true, true));
builder->Write(u"2. ");

ASSERT_EQ(u"2. Hello world! ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world!", doc->GetText().Trim());

// 2 -  All'interno del segnalibro, proprio davanti al nodo BookmarkEnd:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, false));
builder->Write(u"3. ");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3.", doc->GetText().Trim());

// 4 -  Fuori dal segnalibro, dopo il nodo BookmarkEnd:
ASSERT_TRUE(builder->MoveToBookmark(u"MyBookmark", false, true));
builder->Write(u"4.");

ASSERT_EQ(u"2. Hello world! 3. ", doc->get_Range()->get_Bookmarks()->idx_get(u"MyBookmark")->get_Text());
ASSERT_EQ(u"1. 2. Hello world! 3. 4.", doc->GetText().Trim());
```

## Vedi anche

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
