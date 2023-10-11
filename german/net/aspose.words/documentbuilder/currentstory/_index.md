---
title: DocumentBuilder.CurrentStory
second_title: Aspose.Words für .NET-API-Referenz
description: DocumentBuilder eigendom. Ruft die aktuell ausgewählte Story abDocumentBuilder .
type: docs
weight: 70
url: /de/net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

Ruft die aktuell ausgewählte Story ab[`DocumentBuilder`](../) .

```csharp
public Story CurrentStory { get; }
```

### Beispiele

Zeigt, wie mit der aktuellen Story eines Document Builders gearbeitet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Story ist ein Knotentyp, der untergeordnete Absatzknoten hat, z. B. einen Textkörper.
Assert.AreEqual(builder.CurrentStory, doc.FirstSection.Body);
Assert.AreEqual(builder.CurrentStory, builder.CurrentParagraph.ParentNode);
Assert.AreEqual(StoryType.MainText, builder.CurrentStory.StoryType);

builder.CurrentStory.AppendParagraph("Text added to current Story.");

// Eine Story kann auch Tabellen enthalten.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndTable();

Assert.IsTrue(builder.CurrentStory.Tables.Contains(table));
```

### Siehe auch

* class [Story](../../story/)
* class [DocumentBuilder](../)
* namensraum [Aspose.Words](../../documentbuilder/)
* Montage [Aspose.Words](../../../)


