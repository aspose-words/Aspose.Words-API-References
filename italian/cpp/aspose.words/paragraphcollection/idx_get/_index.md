---
title: "Aspose::Words::ParagraphCollection::idx_get metodo"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ParagraphCollection::idx_get metodo. Recupera un Paragraph all'indice specificato in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/paragraphcollection/idx_get/
---
## ParagraphCollection::idx_get method


Recupera un [Paragraph](../../paragraph/) all'indice specificato.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::ParagraphCollection::idx_get(int32_t index)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| index | int32_t | Un indice nella collezione. |
## Note


L'indice parte da zero.

Gli indici negativi sono consentiti e indicano l'accesso dalla fine della collezione. Per esempio, -1 indica l'ultimo elemento, -2 il penultimo e così via.

Se l'indice è maggiore o uguale al numero di elementi nella lista, questo restituisce un riferimento nullo.

Se l'indice è negativo e il suo valore assoluto è maggiore del numero di elementi nella lista, questo restituisce un riferimento nullo.

## Esempi



Mostra come verificare se un paragrafo è una revisione di spostamento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Questo documento contiene revisioni "Move", che appaiono quando evidenziamo il testo con il cursore,
// e poi lo trasciniamo per spostarlo in un'altra posizione
// mentre tracciamo le revisioni in Microsoft Word tramite "Review" -> "Track changes".
ASSERT_EQ(6, doc->get_Revisions()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Revision>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Revision> r)>>([](System::SharedPtr<Aspose::Words::Revision> r) -> bool
{
    return r->get_RevisionType() == Aspose::Words::RevisionType::Moving;
}))));

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// Le revisioni di spostamento consistono in coppie di revisioni "Move from" e "Move to".
// Queste revisioni sono modifiche potenziali al documento che possiamo accettare o rifiutare.
// Prima di accettare/rifiutare una revisione di spostamento, il documento
// deve tenere traccia sia della destinazione di partenza sia di quella di arrivo del testo.
// Il secondo e il quarto paragrafo definiscono una tale revisione, e quindi entrambi hanno lo stesso contenuto.
ASSERT_EQ(paragraphs->idx_get(1)->GetText(), paragraphs->idx_get(3)->GetText());

// La revisione "Move from" è il paragrafo da cui abbiamo trascinato il testo.
// Se accettiamo la revisione, questo paragrafo scomparirà,
// e l'altro rimarrà e non sarà più una revisione.
ASSERT_TRUE(paragraphs->idx_get(1)->get_IsMoveFromRevision());

// La revisione "Move to" è il paragrafo verso cui abbiamo trascinato il testo.
// Se rifiutiamo la revisione, questo paragrafo invece scomparirà, e l'altro rimarrà.
ASSERT_TRUE(paragraphs->idx_get(3)->get_IsMoveToRevision());
```

## Vedi anche

* Class [Paragraph](../../paragraph/)
* Class [ParagraphCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
