---
title: "Aspose::Words::DocumentBuilder::MoveToParagraph metodo"
linktitle: "MoveToParagraph"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::MoveToParagraph metodo. Sposta il cursore a un paragrafo nella sezione corrente in C++."
type: docs
weight: 59000
url: /it/cpp/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder::MoveToParagraph method


Sposta il cursore su un paragrafo nella sezione corrente.

```cpp
void Aspose::Words::DocumentBuilder::MoveToParagraph(int32_t paragraphIndex, int32_t characterIndex)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| paragraphIndex | int32_t | L'indice del paragrafo a cui spostarsi. |
| characterIndex | int32_t | L'indice del carattere all'interno del paragrafo. Un valore negativo consente di specificare una posizione dalla fine del paragrafo. Usa -1 per spostarti alla fine del paragrafo. |
## Note


La navigazione viene eseguita all'interno della storia corrente della sezione corrente. Cioè, se hai spostato il cursore sull'intestazione primaria della prima sezione, allora *paragraphIndex* specifica l'indice del paragrafo all'interno di quell'intestazione di quella sezione.

Quando *paragraphIndex* è maggiore o uguale a 0, specifica un indice dall'inizio della sezione, con 0 che rappresenta il primo paragrafo. Quando *paragraphIndex* è minore di 0, specifica un indice dalla fine della sezione, con -1 che rappresenta l'ultimo paragrafo.

## Esempi



Mostra come spostare la posizione del cursore del builder a un paragrafo specificato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(22, paragraphs->get_Count());

// Crea un document builder per modificare il documento. Il cursore del builder,
// che è il punto in cui inserirà nuovi nodi quando chiamiamo i suoi metodi di costruzione del documento,
// si trova attualmente all'inizio del documento.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_EQ(0, paragraphs->IndexOf(builder->get_CurrentParagraph()));

// Spostare quel cursore a un paragrafo diverso lo posizionerà davanti a quel paragrafo.
builder->MoveToParagraph(2, 0);

// Qualsiasi nuovo contenuto che aggiungiamo verrà inserito in quel punto.
builder->Writeln(u"This is a new third paragraph. ");
```

## Vedi anche

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
