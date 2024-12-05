---
title: BaselineAlignment Enum
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words for .NET
description: Aspose.Words.BaselineAlignment enum. Specifies fonts vertical position on a line in C#.
type: docs
weight: 110
url: /net/aspose.words/baselinealignment/
---
## BaselineAlignment enumeration

Specifies fonts vertical position on a line.

```csharp
public enum BaselineAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Top | `0` | Aligns along the top of each font. |
| Center | `1` | Aligns the center points of each font. |
| Baseline | `2` | Aligns to the baseline of the paragraph. |
| Bottom | `3` | Aligns to the bottom of each font. |
| Auto | `4` | Baseline is adjusted automatically. |

## Examples

Shows how to set fonts vertical position on a line.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
if (format.BaselineAlignment == BaselineAlignment.Auto)
{                
    format.BaselineAlignment = BaselineAlignment.Top;
}

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
