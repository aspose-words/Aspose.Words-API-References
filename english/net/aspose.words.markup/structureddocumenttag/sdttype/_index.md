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

Assert.That(tags[0].SdtType, Is.EqualTo(SdtType.RepeatingSection));
Assert.That(tags[1].SdtType, Is.EqualTo(SdtType.RepeatingSectionItem));
Assert.That(tags[2].SdtType, Is.EqualTo(SdtType.RichText));
```

### See Also

* enum [SdtType](../../sdttype/)
* class [StructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
