---
title: "Aspose::Words::ParagraphCollection Klasse"
linktitle: "ParagraphCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphCollection Klasse. Bietet typisierten Zugriff auf eine Sammlung von Paragraph‑Knoten. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 48000
url: /de/cpp/aspose.words/paragraphcollection/
---
## ParagraphCollection class


Bietet typisierten Zugriff auf eine Sammlung von [Paragraph](../paragraph/)-Knoten. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class ParagraphCollection : public Aspose::Words::NodeCollection
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
| [idx_get](./idx_get/)(int32_t) | Ruft ein [Paragraph](../paragraph/) am angegebenen Index ab. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Gibt den nullbasierten Index des angegebenen Knotens zurück. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Fügt einen Knoten in die Sammlung am angegebenen Index ein. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Entfernt den Knoten aus der Sammlung und aus dem Dokument. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Entfernt den Knoten am angegebenen Index aus der Sammlung und aus dem Dokument. |
| [ToArray](./toarray/)() | Kopiert alle Absätze aus der Sammlung in ein neues Array von Absätzen. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man prüft, ob ein Absatz eine Verschiebungsrevision ist.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Dieses Dokument enthält "Move"-Revisionen, die erscheinen, wenn wir Text mit dem Cursor markieren,
// und ihn dann ziehen, um ihn an einen anderen Ort zu verschieben
// während wir Revisionen in Microsoft Word über "Review" -> "Track changes" verfolgen.
ASSERT_EQ(6, doc->get_Revisions()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Revision>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Revision> r)>>([](System::SharedPtr<Aspose::Words::Revision> r) -> bool
{
    return r->get_RevisionType() == Aspose::Words::RevisionType::Moving;
}))));

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// Verschiebungsrevisionen bestehen aus Paaren von "Move from"- und "Move to"-Revisionen.
// Diese Revisionen sind potenzielle Änderungen am Dokument, die wir entweder akzeptieren oder ablehnen können.
// Bevor wir eine Verschiebungsrevision akzeptieren/ablehnen, muss das Dokument
// sowohl die Abgangs- als auch die Ankunftsposition des Textes verfolgen.
// Der zweite und der vierte Absatz definieren eine solche Revision, und daher haben beide denselben Inhalt.
ASSERT_EQ(paragraphs->idx_get(1)->GetText(), paragraphs->idx_get(3)->GetText());

// Die "Move from"-Revision ist der Absatz, von dem wir den Text gezogen haben.
// Wenn wir die Revision akzeptieren, wird dieser Absatz verschwinden,
// und der andere bleibt erhalten und ist keine Revision mehr.
ASSERT_TRUE(paragraphs->idx_get(1)->get_IsMoveFromRevision());

// Die "Move to"-Revision ist der Absatz, zu dem wir den Text gezogen haben.
// Wenn wir die Revision ablehnen, wird dieser Absatz stattdessen verschwinden, und der andere bleibt erhalten.
ASSERT_TRUE(paragraphs->idx_get(3)->get_IsMoveToRevision());
```

## Siehe auch

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
