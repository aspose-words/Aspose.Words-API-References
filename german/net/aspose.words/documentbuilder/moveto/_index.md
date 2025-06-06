---
title: DocumentBuilder.MoveTo
linktitle: MoveTo
articleTitle: MoveTo
second_title: Aspose.Words für .NET
description: Entdecken Sie die MoveTo-Methode von DocumentBuilder, um problemlos durch Inline-Knoten zu navigieren und Ihren Cursor effizient an Absatzenden zu positionieren, um Dokumente nahtlos zu bearbeiten.
type: docs
weight: 520
url: /de/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

Bewegt den Cursor zu einem Inline-Knoten oder an das Ende eines Absatzes.

```csharp
public void MoveTo(Node node)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| node | Node | Der Knoten muss ein Absatz oder ein direktes untergeordnetes Element eines Absatzes sein. |

## Bemerkungen

WannKnoten ist ein Knoten auf Inline-Ebene, der Cursor wird zu diesem Knoten bewegt und weiterer Inhalt wird vor diesem Knoten eingefügt.

WannKnoten ist ein[`Paragraph`](../../paragraph/)wird der Cursor an das Ende des Absatzes bewegt und weiterer Inhalt wird unmittelbar vor dem Absatzumbruch eingefügt.

WannKnoten ist ein Blockknoten, aber kein[`Paragraph`](../../paragraph/)wird der Cursor an das Ende des ersten Absatzes in den Block-Level-Knoten node verschoben und weiterer Inhalt wird direkt vor dem Absatzumbruch eingefügt.

## Beispiele

Zeigt, wie die Cursorposition eines DocumentBuilder zu einem angegebenen Knoten verschoben wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Der Dokument-Builder verfügt über einen Cursor, der als Teil des Dokuments fungiert
// wo der Builder neue Knoten anfügt, wenn wir seine Methoden zur Dokumenterstellung verwenden.
// Dieser Cursor funktioniert auf die gleiche Weise wie der blinkende Cursor von Microsoft Word.
// und es endet auch immer unmittelbar nach einem Knoten, den der Builder gerade eingefügt hat.
// Um Inhalt an einen anderen Teil des Dokuments anzuhängen,
// Wir können den Cursor mit der Methode „MoveTo“ zu einem anderen Knoten verschieben.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// Der Cursor steht jetzt vor dem Knoten, zu dem wir ihn verschoben haben.
// Wenn Sie einen zweiten Lauf hinzufügen, wird dieser vor dem ersten Lauf eingefügt.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Bewegen Sie den Cursor an das Ende des Dokuments, um wie zuvor mit dem Anhängen von Text am Ende fortzufahren.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

Zeigt, wie der Cursor eines Dokument-Generators zu verschiedenen Knoten in einem Dokument bewegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstelle ein gültiges Lesezeichen, eine Entität, die aus Knoten besteht, die von einem Lesezeichen-Startknoten umschlossen sind,
    // und ein Lesezeichen-Endknoten.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Der Cursor des Dokumentgenerators befindet sich immer vor dem Knoten, den wir zuletzt damit hinzugefügt haben.
// Wenn sich der Cursor des Builders am Ende des Dokuments befindet, ist sein aktueller Knoten null.
// Der vorherige Knoten ist der Lesezeichen-Endknoten, den wir zuletzt hinzugefügt haben.
// Wenn Sie mit dem Builder neue Knoten hinzufügen, werden diese an den letzten Knoten angehängt.
Assert.Null(builder.CurrentNode);

// Wenn wir einen anderen Teil des Dokuments mit dem Builder bearbeiten möchten,
// Wir müssen den Cursor auf den Knoten bewegen, den wir bearbeiten möchten.
builder.MoveToBookmark("MyBookmark");

// Durch Verschieben in ein Lesezeichen wird es zum ersten Knoten innerhalb der Start- und Endknoten des Lesezeichens verschoben, dem eingeschlossenen Lauf.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// Wir können den Cursor auch auf einen einzelnen Knoten wie diesen bewegen.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false)[0]);

Assert.AreEqual(NodeType.BookmarkStart, builder.CurrentNode.NodeType);
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, builder.CurrentParagraph);
Assert.IsTrue(builder.IsAtStartOfParagraph);

// Wir können bestimmte Methoden verwenden, um zum Anfang/Ende eines Dokuments zu gelangen.
builder.MoveToDocumentEnd();

Assert.IsTrue(builder.IsAtEndOfParagraph);

builder.MoveToDocumentStart();

Assert.IsTrue(builder.IsAtStartOfParagraph);
```

### Siehe auch

* class [Node](../../node/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
