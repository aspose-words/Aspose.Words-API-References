---
title: "Aspose::Words::DocumentBuilder::MoveToParagraph-Methode"
linktitle: "MoveToParagraph"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::MoveToParagraph method. Verschiebt den Cursor zu einem Absatz im aktuellen Abschnitt in C++."
type: docs
weight: 59000
url: /de/cpp/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder::MoveToParagraph method


Bewegt den Cursor zu einem Absatz im aktuellen Abschnitt.

```cpp
void Aspose::Words::DocumentBuilder::MoveToParagraph(int32_t paragraphIndex, int32_t characterIndex)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| paragraphIndex | int32_t | Der Index des Absatzes, zu dem gewechselt werden soll. |
| characterIndex | int32_t | Der Index des Zeichens innerhalb des Absatzes. Ein negativer Wert ermöglicht die Angabe einer Position vom Ende des Absatzes aus. Verwenden Sie -1, um zum Ende des Absatzes zu springen. |
## Hinweise


Die Navigation wird innerhalb der aktuellen Story des aktuellen Abschnitts durchgeführt. Das heißt, wenn Sie den Cursor zur primären Kopfzeile des ersten Abschnitts verschoben haben, dann gibt *paragraphIndex* den Index des Absatzes innerhalb dieser Kopfzeile dieses Abschnitts an.

Wenn *paragraphIndex* größer oder gleich 0 ist, gibt er einen Index vom Anfang des Abschnitts an, wobei 0 der erste Absatz ist. Wenn *paragraphIndex* kleiner als 0 ist, gibt er einen Index vom Ende des Abschnitts an, wobei -1 der letzte Absatz ist.

## Beispiele



Zeigt, wie die Cursorposition eines Builders zu einem angegebenen Absatz verschoben wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(22, paragraphs->get_Count());

// Erstellen Sie einen DocumentBuilder, um das Dokument zu bearbeiten. Der Cursor des Builders,
// der der Punkt ist, an dem neue Knoten eingefügt werden, wenn wir seine Dokumenterstellungsmethoden aufrufen,
// befindet sich derzeit am Anfang des Dokuments.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

ASSERT_EQ(0, paragraphs->IndexOf(builder->get_CurrentParagraph()));

// Das Verschieben dieses Cursors zu einem anderen Absatz positioniert den Cursor vor diesem Absatz.
builder->MoveToParagraph(2, 0);

// Jeglicher neue Inhalt, den wir hinzufügen, wird an dieser Stelle eingefügt.
builder->Writeln(u"This is a new third paragraph. ");
```

## Siehe auch

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
