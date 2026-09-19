---
title: "Classe Aspose::Words::CommentCollection"
linktitle: "CommentCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::CommentCollection. Fornisce accesso tipizzato a una collezione di nodi Comment. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words/commentcollection/
---
## CommentCollection class


Fornisce accesso tipizzato a una collezione di nodi [Comment](../comment/). Per saperne di più, visita l'articolo di documentazione [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class CommentCollection : public Aspose::Words::NodeCollection
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
| [idx_get](./idx_get/)(int32_t) | Recupera un [Comment](../comment/) all'indice specificato. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Restituisce l'indice basato su zero del nodo specificato. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserisce un nodo nella collezione all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Rimuove il nodo dalla raccolta e dal documento. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Rimuove il nodo all'indice specificato dalla raccolta e dal documento. |
| [ToArray](../nodecollection/toarray/)() | Copia tutti i nodi dalla raccolta in un nuovo array di nodi. |
| static [Type](./type/)() |  |

## Esempi



Mostra come contrassegnare un commento come "done".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// Inserisci un commento per evidenziare un errore.
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// I commenti hanno un flag "Done", che è impostato su "false" per impostazione predefinita.
// Se un commento suggerisce di apportare una modifica all'interno del documento,
// possiamo applicare la modifica e poi impostare il flag "Done" per indicare la correzione.
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// I commenti che sono "done" si differenzieranno
// da quelli che non sono "completati" con un colore del testo sbiadito.
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## Vedi anche

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
