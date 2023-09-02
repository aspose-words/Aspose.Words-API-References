---
title: ParagraphFormat.BaselineAlignment
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words for .NET
description: ParagraphFormat BaselineAlignment property. Gets or sets fonts vertical position on a line in C#.
type: docs
weight: 40
url: /net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

Gets or sets fonts vertical position on a line.

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

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

* enum [BaselineAlignment](../../baselinealignment/)
* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
