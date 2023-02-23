---
title: DocumentBuilder.IsAtEndOfStructuredDocumentTag
linktitle: IsAtEndOfStructuredDocumentTag
second_title: Aspose.Words for .NET API Reference
description: DocumentBuilder property. Returns true if the cursor is at the end of a structured document tag in C#.
type: docs
weight: 120
url: /net/aspose.words/documentbuilder/isatendofstructureddocumenttag/
---
## DocumentBuilder.IsAtEndOfStructuredDocumentTag property

Returns **true** if the cursor is at the end of a structured document tag.

```csharp
public bool IsAtEndOfStructuredDocumentTag { get; }
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

* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)
