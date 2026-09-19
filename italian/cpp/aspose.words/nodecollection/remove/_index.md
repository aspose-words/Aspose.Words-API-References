---
title: "Metodo Aspose::Words::NodeCollection::Remove"
linktitle: "Rimuovi"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::NodeCollection::Remove. Rimuove il nodo dalla raccolta e dal documento in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words/nodecollection/remove/
---
## NodeCollection::Remove method


Rimuove il nodo dalla raccolta e dal documento.

```cpp
void Aspose::Words::NodeCollection::Remove(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nodo | const System::SharedPtr\<Aspose::Words::Node\>\& | Il nodo da rimuovere. |

## Esempi



Mostra come lavorare con una [NodeCollection](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aggiungi testo al documento inserendo Run usando un DocumentBuilder.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");

// Ogni invocazione del metodo "Write" crea un nuovo Run,
// che poi appare nella RunCollection del Paragraph genitore.
System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_EQ(2, runs->get_Count());

// Possiamo anche inserire manualmente un nodo nella RunCollection.
auto newRun = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");
runs->Insert(3, newRun);

ASSERT_TRUE(runs->Contains(newRun));
ASSERT_EQ(u"Run 1. Run 2. Run 3.", doc->GetText().Trim());

// Accedi ai singoli run e rimuovili per eliminare il loro testo dal documento.
System::SharedPtr<Aspose::Words::Run> run = runs->idx_get(1);
runs->Remove(run);

ASSERT_EQ(u"Run 1. Run 3.", doc->GetText().Trim());
ASSERT_FALSE(System::TestTools::IsNull(run));
ASSERT_FALSE(runs->Contains(run));
```

## Vedi anche

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
