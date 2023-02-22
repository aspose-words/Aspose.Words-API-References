---
title: DocumentBuilder.MoveTo
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder methode. Bewegt den Cursor zu einem InlineKnoten oder zum Ende eines Absatzes.
type: docs
weight: 460
url: /de/net/aspose.words/documentbuilder/moveto/
---
## DocumentBuilder.MoveTo method

Bewegt den Cursor zu einem Inline-Knoten oder zum Ende eines Absatzes.

```csharp
public void MoveTo(Node node)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| node | Node | Der Knoten muss ein Absatz oder ein direktes Kind eines Absatzes sein. |

### Bemerkungen

WannKnoten ein Inline-Level-Knoten ist, wird der Cursor zu diesem Knoten bewegt und weitere Inhalte werden vor diesem Knoten eingefügt.

WannKnoten ist ein **Absatz**, wird der Cursor an das Ende des Absatzes bewegt und weitere Inhalte werden kurz vor dem Absatzumbruch eingefügt.

WannKnotenein Knoten auf Blockebene, aber kein Absatz ist, wird der Cursor an das Ende des ersten Absatzes in den Blockknoten node bewegt und weiterer Inhalt wird unmittelbar vor dem Absatzumbruch eingefügt.

### Beispiele

Zeigt, wie die Cursorposition eines DocumentBuilder zu einem angegebenen Knoten verschoben wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Der Document Builder hat einen Cursor, der als Teil des Dokuments fungiert
// wo der Builder neue Knoten anfügt, wenn wir seine Dokumentkonstruktionsmethoden verwenden.
// Dieser Cursor funktioniert genauso wie der blinkende Cursor von Microsoft Word,
// und es endet auch immer unmittelbar nach jedem Knoten, den der Builder gerade eingefügt hat.
// Um Inhalt an einen anderen Teil des Dokuments anzuhängen,
// Mit der Methode "MoveTo" können wir den Cursor zu einem anderen Knoten bewegen.
// Der Cursor steht jetzt vor dem Knoten, zu dem wir ihn verschoben haben.
// Wenn Sie einen zweiten Lauf hinzufügen, wird dieser vor dem ersten Lauf eingefügt.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Bewegen Sie den Cursor an das Ende des Dokuments, um wie zuvor mit dem Anhängen von Text an das Ende fortzufahren.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

Zeigt, wie der Cursor eines Document Builder zu verschiedenen Knoten in einem Dokument bewegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein gültiges Lesezeichen, eine Entität, die aus Knoten besteht, die von einem Lesezeichen-Startknoten eingeschlossen sind,
 // und ein Lesezeichen-Endknoten.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.ChildNodes;

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Der Cursor des Document Builder steht immer vor dem Knoten, den wir zuletzt mit ihm hinzugefügt haben.
// Wenn sich der Cursor des Builders am Ende des Dokuments befindet, ist sein aktueller Knoten null.
// Der vorherige Knoten ist der Lesezeichen-Endknoten, den wir zuletzt hinzugefügt haben.
// Wenn Sie neue Knoten mit dem Builder hinzufügen, werden sie an den letzten Knoten angehängt.
Assert.Null(builder.CurrentNode);

// Wenn wir einen anderen Teil des Dokuments mit dem Builder bearbeiten möchten,
// Wir müssen den Cursor auf den Knoten bringen, den wir bearbeiten möchten.
builder.MoveToBookmark("MyBookmark");

// Wenn Sie es zu einem Lesezeichen verschieben, wird es zum ersten Knoten innerhalb der Start- und Endknoten des Lesezeichens verschoben, dem eingeschlossenen Lauf.
Assert.AreEqual(firstParagraphNodes[1], builder.CurrentNode);

// Wir können den Cursor auch so auf einen einzelnen Knoten bewegen.
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
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


