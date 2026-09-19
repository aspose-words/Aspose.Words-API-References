---
title: "Aspose::Words::Body::EnsureMinimum metodo"
linktitle: "EnsureMinimum"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Body::EnsureMinimum metodo. Se l'ultimo figlio non è un paragrafo, crea e aggiunge un paragrafo vuoto in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/body/ensureminimum/
---
## Body::EnsureMinimum method


Se l'ultimo figlio non è un paragrafo, crea e aggiunge un paragrafo vuoto.

```cpp
void Aspose::Words::Body::EnsureMinimum()
```


## Esempi



Cancella il testo principale da tutte le sezioni del documento lasciando intatte le sezioni stesse.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento vuoto contiene una sezione, un corpo e un paragrafo.
// Chiama il metodo "RemoveAllChildren" per rimuovere tutti quei nodi,
// e otterrai un nodo documento senza figli.
doc->RemoveAllChildren();

// Questo documento ora non ha nodi figli compositi a cui possiamo aggiungere contenuti.
// Se desideriamo modificarlo, dovremo ripopolare la sua collezione di nodi.
// Per prima cosa, crea una nuova sezione, quindi aggiungila come figlio al nodo radice del documento.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Una sezione ha bisogno di un corpo, che conterrà e visualizzerà tutti i suoi contenuti
// sulla pagina tra l'intestazione e il piè di pagina della sezione.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Questo body non ha figli, quindi non possiamo ancora aggiungere run.
ASSERT_EQ(0, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Chiama \"EnsureMinimum\" per assicurarti che questo body contenga almeno un paragrafo vuoto.
body->EnsureMinimum();

// Ora possiamo aggiungere run al body e far visualizzare il documento.
body->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Vedi anche

* Class [Body](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
