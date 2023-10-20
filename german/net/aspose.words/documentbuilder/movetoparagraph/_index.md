---
title: DocumentBuilder.MoveToParagraph
linktitle: MoveToParagraph
articleTitle: MoveToParagraph
second_title: Aspose.Words für .NET
description: DocumentBuilder MoveToParagraph methode. Bewegt den Cursor zu einem Absatz im aktuellen Abschnitt in C#.
type: docs
weight: 560
url: /de/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

Bewegt den Cursor zu einem Absatz im aktuellen Abschnitt.

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| paragraphIndex | Int32 | Der Index des Absatzes, zu dem verschoben werden soll. |
| characterIndex | Int32 | Der Index des Zeichens innerhalb des Absatzes. Mit einem negativen Wert können Sie eine Position ab dem Ende des Absatzes angeben. Verwenden Sie -1, um zum Ende des Absatzes zu gelangen. |

## Bemerkungen

Die Navigation erfolgt innerhalb der aktuellen Story des aktuellen Abschnitts. Das heißt, wenn Sie den Cursor auf die primäre Kopfzeile des ersten Abschnitts bewegt haben, dann*paragraphIndex*gab den Index des Absatzes innerhalb des header dieses Abschnitts an.

Wann*paragraphIndex* größer oder gleich 0 ist, gibt es einen Index ab dem Anfang des Abschnitts an, wobei 0 der erste Absatz ist. Wann*paragraphIndex* kleiner als 0, ist, wurde ein Index vom Ende des Abschnitts angegeben, wobei -1 der letzte Absatz ist.

## Beispiele

Zeigt, wie die Cursorposition eines Builders auf einen bestimmten Absatz verschoben wird.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Dokument-Builder erstellen, um das Dokument zu bearbeiten. Der Cursor des Erbauers,
// Das ist der Punkt, an dem neue Knoten eingefügt werden, wenn wir seine Dokumentkonstruktionsmethoden aufrufen.
// steht derzeit am Anfang des Dokuments.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// Wenn Sie den Cursor auf einen anderen Absatz bewegen, wird dieser Cursor vor diesem Absatz platziert.
builder.MoveToParagraph(2, 0);
// Jeder neue Inhalt, den wir hinzufügen, wird an dieser Stelle eingefügt.
builder.Writeln("This is a new third paragraph. ");
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
