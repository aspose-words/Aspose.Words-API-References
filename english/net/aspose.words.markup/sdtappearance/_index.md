---
title: SdtAppearance Enum
linktitle: SdtAppearance
articleTitle: SdtAppearance
second_title: Aspose.Words for .NET
description: Aspose.Words.Markup.SdtAppearance enum. Specifies the appearance of a structured document tag in C#.
type: docs
weight: 4150
url: /net/aspose.words.markup/sdtappearance/
---
## SdtAppearance enumeration

Specifies the appearance of a structured document tag.

```csharp
public enum SdtAppearance
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| BoundingBox | `0` | Represents a structured document tag shown as a shaded rectangle or bounding box. |
| Tags | `1` | Represents a structured document tag shown as start and end markers. |
| Hidden | `2` | Represents a structured document tag that is not shown. |
| Default | `0` | Defaults to BoundingBox. |

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

* namespace [Aspose.Words.Markup](../../aspose.words.markup/)
* assembly [Aspose.Words](../../)
