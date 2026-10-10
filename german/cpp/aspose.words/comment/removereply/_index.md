---
title: "Aspose::Words::Comment::RemoveReply Methode"
linktitle: "RemoveReply"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Comment::RemoveReply Methode. Entfernt die angegebene Antwort auf diesen Kommentar in C++."
type: docs
weight: 17000
url: /de/cpp/aspose.words/comment/removereply/
---
## Comment::RemoveReply method


Entfernt die angegebene Antwort auf diesen Kommentar.

```cpp
void Aspose::Words::Comment::RemoveReply(const System::SharedPtr<Aspose::Words::Comment> &reply)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Antwort | const System::SharedPtr\<Aspose::Words::Comment\>\& | Der Kommentar-Knoten der zu löschenden Antwort. |

## Beispiele



Zeigt, wie man Kommentarantworten entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"Another reply");

ASSERT_EQ(2, comment->get_Replies()->get_Count());

// Unten sind zwei Möglichkeiten, Antworten von einem Kommentar zu entfernen.
// 1 -  Verwenden Sie die Methode "RemoveReply", um Antworten von einem Kommentar einzeln zu entfernen:
comment->RemoveReply(comment->get_Replies()->idx_get(0));

ASSERT_EQ(1, comment->get_Replies()->get_Count());

// 2 -  Verwenden Sie die Methode "RemoveAllReplies", um alle Antworten von einem Kommentar auf einmal zu entfernen:
comment->RemoveAllReplies();

ASSERT_EQ(0, comment->get_Replies()->get_Count());
```

## Siehe auch

* Class [Comment](../)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
