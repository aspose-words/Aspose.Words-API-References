---
title: "Metodo Aspose::Words::Comment::RemoveAllReplies"
linktitle: "RemoveAllReplies"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Comment::RemoveAllReplies. Rimuove tutte le risposte a questo commento in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words/comment/removeallreplies/
---
## Comment::RemoveAllReplies method


Rimuove tutte le risposte a questo commento.

```cpp
void Aspose::Words::Comment::RemoveAllReplies()
```


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

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
