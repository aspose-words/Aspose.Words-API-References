---
title: "Aspose::Words::Story::get_LastParagraph metodo"
linktitle: "get_LastParagraph"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Story::get_LastParagraph metodo. Ottiene l'ultimo paragrafo nella storia in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/story/get_lastparagraph/
---
## Story::get_LastParagraph method


Ottiene l'ultimo paragrafo nella storia.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::get_LastParagraph() override
```


## Esempi



Mostra come spostare la posizione del cursore di un [DocumentBuilder](../../documentbuilder/) a un nodo specificato.
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

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
