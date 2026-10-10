---
title: "Classe Aspose::Words::ParagraphCollection"
linktitle: "ParagraphCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::ParagraphCollection. Fornisce accesso tipizzato a una raccolta di nodi Paragraph. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 48000
url: /it/cpp/aspose.words/paragraphcollection/
---
## ParagraphCollection class


Fornisce accesso tipizzato a una raccolta di nodi [Paragraph](../paragraph/). Per saperne di più, visita l'articolo di documentazione [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class ParagraphCollection : public Aspose::Words::NodeCollection
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Aggiunge un nodo alla fine della collezione. |
| [Clear](../nodecollection/clear/)() | Rimuove tutti i nodi da questa collezione e dal documento. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determina se un nodo è nella collezione. |
| [get_Count](../nodecollection/get_count/)() | Ottiene il numero di nodi nella collezione. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Fornisce una semplice iterazione in stile "foreach" sulla collezione di nodi. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Recupera un [Paragraph](../paragraph/) all'indice specificato. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Restituisce l'indice basato su zero del nodo specificato. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserisce un nodo nella collezione all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Rimuove il nodo dalla raccolta e dal documento. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [ToArray](./toarray/)() | Copia tutti i paragrafi dalla raccolta in un nuovo array di paragrafi. |
| static [Type](./type/)() |  |

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

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
