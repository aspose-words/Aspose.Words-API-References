---
title: DocumentBuilder.CurrentStructuredDocumentTag
linktitle: CurrentStructuredDocumentTag
articleTitle: CurrentStructuredDocumentTag
second_title: Aspose.Words for .NET
description: Discover the CurrentStructuredDocumentTag property in DocumentBuilder. Easily access the selected structured document tag for efficient document management.
type: docs
weight: 80
url: /net/aspose.words/documentbuilder/currentstructureddocumenttag/
---
## DocumentBuilder.CurrentStructuredDocumentTag property

Gets the structured document tag that is currently selected in this [`DocumentBuilder`](../).

```csharp
public StructuredDocumentTag CurrentStructuredDocumentTag { get; }
```

## Examples

Shows how to move cursor of DocumentBuilder inside a structured document tag.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// There is a several ways to move the cursor:
// 1 -  Move to the first character of structured document tag by index.
builder.MoveToStructuredDocumentTag(1, 1);

// 2 -  Move to the first character of structured document tag by object.
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 -  Move to the end of the second structured document tag.
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);

// Get currently selected structured document tag.
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### See Also

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
