---
title: DocumentBuilder.MoveToParagraph
linktitle: MoveToParagraph
articleTitle: MoveToParagraph
second_title: Aspose.Words für .NET
description: Navigieren Sie mühelos durch Ihr Dokument mit der MoveToParagraph-Methode von DocumentBuilder und ermöglichen Sie eine schnelle Cursorbewegung zu jedem Absatz in Ihrem Abschnitt.
type: docs
weight: 600
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
| characterIndex | Int32 | Der Index des Zeichens innerhalb des Absatzes. Mit einem negativen Wert können Sie eine Position vom Absatzende aus angeben. Verwenden Sie -1, um zum Ende des Absatzes zu gelangen. |

## Bemerkungen

Die Navigation erfolgt innerhalb der aktuellen Story des aktuellen Abschnitts. Das heißt, wenn Sie den Cursor auf die primäre Überschrift des ersten Abschnitts bewegt haben, dann*paragraphIndex* hat den Index des Absatzes innerhalb der Überschrift dieses Abschnitts angegeben.

Wann*paragraphIndex* größer oder gleich 0 ist, gibt es einen Index von zum Anfang des Abschnitts an, wobei 0 der erste Absatz ist. Wenn*paragraphIndex* ist kleiner als 0, , es wurde ein Index vom Ende des Abschnitts angegeben, wobei -1 der letzte Absatz ist.

## Beispiele

Zeigt, wie die Cursorposition eines Builders zu einem angegebenen Absatz verschoben wird.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Dokument-Builder erstellen, um das Dokument zu bearbeiten. Der Cursor des Builders,
// Dies ist der Punkt, an dem neue Knoten eingefügt werden, wenn wir die Methoden zur Dokumenterstellung aufrufen.
// befindet sich derzeit am Anfang des Dokuments.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// Wenn Sie den Cursor in einen anderen Absatz bewegen, wird der Cursor vor diesem Absatz platziert.
builder.MoveToParagraph(2, 0);
// Alle neuen Inhalte, die wir hinzufügen, werden an dieser Stelle eingefügt.
builder.Writeln("This is a new third paragraph. ");
```

### Siehe auch

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
