---
title: "Aspose::Words::ParagraphCollection::idx_get Methode"
linktitle: "idx_get"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphCollection::idx_get Methode. Ruft einen Absatz am angegebenen Index in C++ ab."
type: docs
weight: 3000
url: /de/cpp/aspose.words/paragraphcollection/idx_get/
---
## ParagraphCollection::idx_get method


Ruft einen [Paragraph](../../paragraph/) am angegebenen Index ab.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::ParagraphCollection::idx_get(int32_t index)
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

* Class [Paragraph](../../paragraph/)
* Class [ParagraphCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
