---
title: "Metodo Aspose::Words::Node::Clone"
linktitle: "Clone"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Node::Clone. Crea un duplicato del nodo in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/node/clone/
---
## Node::Clone method


Crea un duplicato del nodo.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::Clone(bool isCloneChildren)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| isCloneChildren | bool | True per clonare ricorsivamente il sottoalbero sotto il nodo specificato; false per clonare solo il nodo stesso. |

### ReturnValue

Il nodo clonato.
## Note


Questo metodo funge da costruttore di copia per i nodi. Il nodo clonato non ha genitore, ma appartiene allo stesso documento del nodo originale.

Questo metodo esegue sempre una copia profonda del nodo. Il parametro *isCloneChildren* specifica se copiare anche tutti i nodi figli.

## Esempi



Mostra come clonare un nodo composito.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Di seguito sono riportati due modi per clonare un nodo composito.
// 1 -  Crea una copia di un nodo e crea anche una copia di ciascuno dei suoi nodi figlio.
System::SharedPtr<Aspose::Words::Node> cloneWithChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(true);

ASSERT_TRUE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithChildren))->get_HasChildNodes());
ASSERT_EQ(u"Hello world!", cloneWithChildren->GetText().Trim());

// 2 -  Crea una copia di un nodo da solo, senza alcun figlio.
System::SharedPtr<Aspose::Words::Node> cloneWithoutChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(false);

ASSERT_FALSE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithoutChildren))->get_HasChildNodes());
ASSERT_EQ(System::String::Empty, cloneWithoutChildren->GetText().Trim());
```

## Vedi anche

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
