---
title: "Metodo Aspose::Words::NodeCollection::Insert"
linktitle: "Inserisci"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::NodeCollection::Insert. Inserisce un nodo nella collezione all'indice specificato in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words/nodecollection/insert/
---
## NodeCollection::Insert method


Inserisce un nodo nella collezione all'indice specificato.

```cpp
void Aspose::Words::NodeCollection::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Node> &node)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | L'indice basato su zero del nodo. Sono consentiti indici negativi e indicano l'accesso dalla fine dell'elenco. Ad esempio, -1 indica l'ultimo nodo, -2 il penultimo e così via. |
| nodo | const System::SharedPtr\<Aspose::Words::Node\>\& | Il nodo da inserire. |
## Note


Il nodo viene inserito come figlio nell'oggetto nodo da cui è stata creata la collezione.

Se l'indice è uguale o maggiore di [Count](../get_count/), il nodo viene aggiunto alla fine della collezione.

Se l'indice è negativo e il suo valore assoluto è maggiore di [Count](../get_count/), il nodo viene aggiunto alla fine della collezione.

Se il nodo da inserire è stato creato da un altro documento, è consigliabile utilizzare [ImportNode()](../) per importare il nodo nel documento corrente. Il nodo importato può quindi essere inserito nel documento corrente.

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
