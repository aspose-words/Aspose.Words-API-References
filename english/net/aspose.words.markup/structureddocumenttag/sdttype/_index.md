---
title: StructuredDocumentTag.SdtType
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words for .NET
description: Discover the SdtType property of StructuredDocumentTag to easily identify tag types, enhancing your document management and organization.
type: docs
weight: 250
url: /net/aspose.words.markup/structureddocumenttag/sdttype/
---
## StructuredDocumentTag.SdtType property

Gets type of this **Structured document tag**.

```csharp
public SdtType SdtType { get; }
```

## Examples

Shows how to get the type of a structured document tag.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.AreEqual(SdtType.RepeatingSection, tags[0].SdtType);
Assert.AreEqual(SdtType.RepeatingSectionItem, tags[1].SdtType);
Assert.AreEqual(SdtType.RichText, tags[2].SdtType);
```

### See Also

* enum [SdtType](../../sdttype/)
* class [StructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
