---
title: "Aspose::Words::Section::get_Body metodo"
linktitle: "get_Body"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Section::get_Body metodo. Restituisce il nodo figlio Body della sezione in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words/section/get_body/
---
## Section::get_Body method


Restituisce il nodo figlio [Body](../../body/) della sezione.

```cpp
System::SharedPtr<Aspose::Words::Body> Aspose::Words::Section::get_Body()
```

## Note


[Body](../../body/) contains main text of the section.

Restituisce **null** se la sezione non ha un nodo [Body](../../body/) tra i suoi figli.

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

* Class [Body](../../body/)
* Class [Section](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
