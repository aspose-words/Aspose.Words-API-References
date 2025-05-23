---
title: IStructuredDocumentTag.LockContents
linktitle: LockContents
articleTitle: LockContents
second_title: Aspose.Words for .NET
description: Discover how the IStructuredDocumentTag LockContents property enhances document security by preventing content edits. Ensure your SDT remains intact!
type: docs
weight: 80
url: /net/aspose.words.markup/istructureddocumenttag/lockcontents/
---
## IStructuredDocumentTag.LockContents property

When set to true, this property will prohibit a user from editing the contents of this **SDT**.

```csharp
public bool LockContents { get; set; }
```

## Examples

Shows how to apply editing restrictions to structured document tags.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a plain text structured document tag, which acts as a text box that prompts the user to fill it in.
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Set the "LockContents" property to "true" to prohibit the user from editing this text box's contents.
tag.LockContents = true;
builder.Write("The contents of this structured document tag cannot be edited: ");
builder.InsertNode(tag);

tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// Set the "LockContentControl" property to "true" to prohibit the user from
// deleting this structured document tag manually in Microsoft Word.
tag.LockContentControl = true;

builder.InsertParagraph();
builder.Write("This structured document tag cannot be deleted but its contents can be edited: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Lock.docx");
```

### See Also

* interface [IStructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
