---
title: IStructuredDocumentTag.Appearance
linktitle: Appearance
articleTitle: Appearance
second_title: Aspose.Words for .NET
description: IStructuredDocumentTag Appearance property. Gets or sets the appearance of the structured document tag in C#.
type: docs
weight: 10
url: /net/aspose.words.markup/istructureddocumenttag/appearance/
---
## IStructuredDocumentTag.Appearance property

Gets or sets the appearance of the structured document tag.

```csharp
public SdtAppearance Appearance { get; set; }
```

## Examples

Shows how to show tag around content.

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

if (tag.Appearance == SdtAppearance.Hidden)
    tag.Appearance = SdtAppearance.Tags;
```

### See Also

* enum [SdtAppearance](../../sdtappearance/)
* interface [IStructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
