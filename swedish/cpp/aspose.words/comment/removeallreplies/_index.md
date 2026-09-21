---
title: "Aspose::Words::Comment::RemoveAllReplies metod"
linktitle: "RemoveAllReplies"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Comment::RemoveAllReplies metod. Tar bort alla svar på denna kommentar i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words/comment/removeallreplies/
---
## Comment::RemoveAllReplies method


Tar bort alla svar på denna kommentar.

```cpp
void Aspose::Words::Comment::RemoveAllReplies()
```


## Exempel



Visar hur man tar bort svar på kommentarer.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"Another reply");

ASSERT_EQ(2, comment->get_Replies()->get_Count());

// Nedan följer två sätt att ta bort svar från en kommentar.
// 1 -  Använd metoden "RemoveReply" för att ta bort svar från en kommentar individuellt:
comment->RemoveReply(comment->get_Replies()->idx_get(0));

ASSERT_EQ(1, comment->get_Replies()->get_Count());

// 2 -  Använd metoden "RemoveAllReplies" för att ta bort alla svar från en kommentar på en gång:
comment->RemoveAllReplies();

ASSERT_EQ(0, comment->get_Replies()->get_Count());
```

## Se även

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
