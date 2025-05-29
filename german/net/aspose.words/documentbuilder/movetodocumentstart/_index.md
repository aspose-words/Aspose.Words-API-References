---
title: DocumentBuilder.MoveToDocumentStart
linktitle: MoveToDocumentStart
articleTitle: MoveToDocumentStart
second_title: Aspose.Words für .NET
description: Entdecken Sie die MoveToDocumentStart-Methode von DocumentBuilder, um mühelos zum Anfang Ihres Dokuments zu navigieren und so Ihre Bearbeitungseffizienz zu steigern.
type: docs
weight: 560
url: /de/net/aspose.words/documentbuilder/movetodocumentstart/
---
## DocumentBuilder.MoveToDocumentStart method

Bewegt den Cursor an den Anfang des Dokuments.

```csharp
public void MoveToDocumentStart()
```

## Beispiele

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

* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
