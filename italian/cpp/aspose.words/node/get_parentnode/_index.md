---
title: "Metodo Aspose::Words::Node::get_ParentNode"
linktitle: "get_ParentNode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Node::get_ParentNode. Ottiene il genitore immediato di questo nodo in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words/node/get_parentnode/
---
## Node::get_ParentNode method


Ottiene il genitore immediato di questo nodo.

```cpp
System::SharedPtr<Aspose::Words::CompositeNode> Aspose::Words::Node::get_ParentNode()
```

## Note


Se un nodo è appena stato creato e non è ancora stato aggiunto all'albero, o se è stato rimosso dall'albero, il genitore è **null**.

## Esempi



Mostra come accedere al nodo genitore di un nodo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();

// Aggiungi un nodo Run figlio al primo paragrafo del documento.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

// Il paragrafo è il nodo genitore del nodo run. Possiamo tracciare questa discendenza
// fino al nodo documento, che è la radice dell'albero dei nodi del documento.
ASPOSE_ASSERT_EQ(para, run->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASPOSE_ASSERT_EQ(doc->get_FirstSection(), doc->get_FirstSection()->get_Body()->get_ParentNode());
ASPOSE_ASSERT_EQ(doc, doc->get_FirstSection()->get_ParentNode());
```


Mostra come creare un nodo e impostare il documento proprietario.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Non abbiamo ancora aggiunto questo paragrafo come figlio a nessun nodo composito.
ASSERT_TRUE(System::TestTools::IsNull(para->get_ParentNode()));

// Se un nodo è un tipo di nodo figlio appropriato di un altro nodo composito,
// possiamo collegarlo come figlio solo se entrambi i nodi hanno lo stesso documento proprietario.
// Il documento proprietario è il documento che abbiamo passato al costruttore del nodo.
// Non abbiamo collegato questo paragrafo al documento, quindi il documento non contiene il suo testo.
ASPOSE_ASSERT_EQ(para->get_Document(), doc);
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());

// Poiché il documento possiede questo paragrafo, possiamo applicare uno dei suoi stili al contenuto del paragrafo.
para->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));

// Aggiungi questo nodo al documento, quindi verifica il suo contenuto.
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body(), para->get_ParentNode());
ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Vedi anche

* Class [CompositeNode](../../compositenode/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
