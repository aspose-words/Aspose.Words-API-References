---
title: DocumentBuilder.CurrentNode
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder eigendom. Ruft den Knoten ab der aktuell in diesem DocumentBuilder ausgewählt ist.
type: docs
weight: 40
url: /de/net/aspose.words/documentbuilder/currentnode/
---
## DocumentBuilder.CurrentNode property

Ruft den Knoten ab, der aktuell in diesem DocumentBuilder ausgewählt ist.

```csharp
public Node CurrentNode { get; }
```

### Bemerkungen

`CurrentNode` ist ein Cursor von[`DocumentBuilder`](../) und zeigt auf a[`Node`](../../node/) das ist ein direktes Kind von a[`Paragraph`](../../paragraph/) . Alle Einfügevorgänge, die Sie mit ausführen[`DocumentBuilder`](../) wird vor dem eingefügt`CurrentNode`.

Wenn der aktuelle Absatz leer ist oder der Cursor gerade vor dem Ende eines Absatzes oder eines strukturierten Dokument-Tags positioniert ist,`CurrentNode` kehrt zurück`Null`.

### Beispiele

Zeigt, wie der Cursor eines Document Builders zu verschiedenen Knoten in einem Dokument bewegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstelle ein gültiges Lesezeichen, eine Entität, die aus Knoten besteht, die von einem Lesezeichen-Startknoten umgeben sind.
 // und ein Lesezeichen-Endknoten.
builder.StartBookmark("MyBookmark");
builder.Write("Bookmark contents.");
builder.EndBookmark("MyBookmark");

NodeCollection firstParagraphNodes = doc.FirstSection.Body.FirstParagraph.GetChildNodes(NodeType.Any, false);

Assert.AreEqual(NodeType.BookmarkStart, firstParagraphNodes[0].NodeType);
Assert.AreEqual(NodeType.Run, firstParagraphNodes[1].NodeType);
Assert.AreEqual("Bookmark contents.", firstParagraphNodes[1].GetText().Trim());
Assert.AreEqual(NodeType.BookmarkEnd, firstParagraphNodes[2].NodeType);

// Der Cursor des Document Builders steht immer vor dem Knoten, den wir zuletzt damit hinzugefügt haben.
// Wenn sich der Cursor des Builders am Ende des Dokuments befindet, ist sein aktueller Knoten null.
// Der vorherige Knoten ist der Lesezeichen-Endknoten, den wir zuletzt hinzugefügt haben.
// Durch das Hinzufügen neuer Knoten mit dem Builder werden diese an den letzten Knoten angehängt.
Assert.Null(builder.CurrentNode);

// Wenn wir einen anderen Teil des Dokuments mit dem Builder bearbeiten möchten,
// Wir müssen den Cursor auf den Knoten setzen, den wir bearbeiten möchten.
builder.MoveToBookmark("MyBookmark");

// Wenn Sie es in ein Lesezeichen verschieben, wird es zum ersten Knoten innerhalb der Start- und Endknoten des Lesezeichens verschoben, dem eingeschlossenen Lauf.
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


