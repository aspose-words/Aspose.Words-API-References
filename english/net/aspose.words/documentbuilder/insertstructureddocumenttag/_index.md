---
title: DocumentBuilder.InsertStructuredDocumentTag
linktitle: InsertStructuredDocumentTag
articleTitle: InsertStructuredDocumentTag
second_title: Aspose.Words for .NET
description: Effortlessly enhance your documents with the DocumentBuilder InsertStructuredDocumentTag method. Easily add structured document tags for better organization!
type: docs
weight: 480
url: /net/aspose.words/documentbuilder/insertstructureddocumenttag/
---
## DocumentBuilder.InsertStructuredDocumentTag method

Inserts a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) into the document.

```csharp
public StructuredDocumentTag InsertStructuredDocumentTag(SdtType type)
```

### Return Value

The [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/) node that was just inserted.

## Examples

Shows how to simply insert structured document tag.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveTo(doc.FirstSection.Body.Paragraphs[3]);
// Note, that only following StructuredDocumentTag types are allowed for insertion:
// SdtType.PlainText, SdtType.RichText, SdtType.Checkbox, SdtType.DropDownList,
// SdtType.ComboBox, SdtType.Picture, SdtType.Date.
// Markup level of inserted StructuredDocumentTag will be detected automatically and depends on position being inserted at.
// Added StructuredDocumentTag will inherit paragraph and font formatting from cursor position.
StructuredDocumentTag sdtPlain = builder.InsertStructuredDocumentTag(SdtType.PlainText);

doc.Save(ArtifactsDir + "StructuredDocumentTag.InsertStructuredDocumentTag.docx");
```

### See Also

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* enum [SdtType](../../../aspose.words.markup/sdttype/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
