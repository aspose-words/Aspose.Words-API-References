---
title: "Aspose::Words::CommentCollection class"
linktitle: "CommentCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::CommentCollection class. Bietet typisierten Zugriff auf eine Sammlung von Comment‑Knoten. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words/commentcollection/
---
## CommentCollection class


Bietet typisierten Zugriff auf eine Sammlung von [Comment](../comment/)-Knoten. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class CommentCollection : public Aspose::Words::NodeCollection
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Fügt einen Knoten am Ende der Sammlung hinzu. |
| [Clear](../nodecollection/clear/)() | Entfernt alle Knoten aus dieser Sammlung und aus dem Dokument. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Bestimmt, ob ein Knoten in der Sammlung ist. |
| [get_Count](../nodecollection/get_count/)() | Ermittelt die Anzahl der Knoten in der Sammlung. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Bietet eine einfache \"foreach\"-artige Iteration über die Sammlung von Knoten. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Ruft einen [Comment](../comment/) am angegebenen Index ab. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Fügt einen Knoten in die Sammlung am angegebenen Index ein. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](../nodecollection/toarray/)() | Kopiert alle Knoten aus der Sammlung in ein neues Knotenarray. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man einen Kommentar als "done" markiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// Fügen Sie einen Kommentar ein, um einen Fehler hervorzuheben.
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Kommentare haben ein "Done"-Flag, das standardmäßig auf "false" gesetzt ist.
// Wenn ein Kommentar vorschlägt, dass wir eine Änderung im Dokument vornehmen,
// Wir können die Änderung anwenden und anschließend das "Done"-Flag setzen, um die Korrektur anzuzeigen.
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// Kommentare, die "done" sind, unterscheiden sich
// von denen, die nicht "done" sind, durch eine verblasste Textfarbe.
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## Siehe auch

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
