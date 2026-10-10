---
title: "Metodo Aspose::Words::CommentCollection::idx_get"
linktitle: "idx_get"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::CommentCollection::idx_get. Recupera un Comment all'indice specificato in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/commentcollection/idx_get/
---
## CommentCollection::idx_get method


Recupera un [Comment](../../comment/) all'indice specificato.

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::CommentCollection::idx_get(int32_t index)
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



Mostra come rimuovere le risposte ai commenti.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"Another reply");

ASSERT_EQ(2, comment->get_Replies()->get_Count());

// Di seguito sono riportati due modi per rimuovere le risposte da un commento.
// 1 -  Usa il metodo \"RemoveReply\" per rimuovere le risposte da un commento individualmente:
comment->RemoveReply(comment->get_Replies()->idx_get(0));

ASSERT_EQ(1, comment->get_Replies()->get_Count());

// 2 -  Usa il metodo \"RemoveAllReplies\" per rimuovere tutte le risposte da un commento in una volta sola:
comment->RemoveAllReplies();

ASSERT_EQ(0, comment->get_Replies()->get_Count());
```

## Vedi anche

* Class [Comment](../../comment/)
* Class [CommentCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
