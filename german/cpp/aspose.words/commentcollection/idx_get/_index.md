---
title: "Aspose::Words::CommentCollection::idx_get Methode"
linktitle: "idx_get"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::CommentCollection::idx_get Methode. Ruft einen Comment am angegebenen Index in C++ ab."
type: docs
weight: 3000
url: /de/cpp/aspose.words/commentcollection/idx_get/
---
## CommentCollection::idx_get method


Ruft einen [Comment](../../comment/) am angegebenen Index ab.

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::CommentCollection::idx_get(int32_t index)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Ein Index in die Sammlung. |
## Hinweise


Der Index ist nullbasiert.

Negative Indizes sind erlaubt und bedeuten Zugriff vom Ende der Sammlung. Zum Beispiel bedeutet -1 das letzte Element, -2 das vorletzte und so weiter.

Wenn der Index größer als oder gleich der Anzahl der Elemente in der Liste ist, gibt dies eine Nullreferenz zurück.

Wenn der Index negativ ist und sein absoluter Wert größer ist als die Anzahl der Elemente in der Liste, gibt dies eine Nullreferenz zurück.

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

* Class [Comment](../../comment/)
* Class [CommentCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
