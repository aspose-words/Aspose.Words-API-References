---
title: ParagraphFormat.FarEastLineBreakControl
linktitle: FarEastLineBreakControl
articleTitle: FarEastLineBreakControl
second_title: Aspose.Words for .NET
description: ParagraphFormat FarEastLineBreakControl property. Gets or sets a flag indicating whether East Asian linebreaking rules are applied to the current paragraph in C#.
type: docs
weight: 110
url: /net/aspose.words/paragraphformat/fareastlinebreakcontrol/
---
## ParagraphFormat.FarEastLineBreakControl property

Gets or sets a flag indicating whether East Asian line-breaking rules are applied to the current paragraph.

```csharp
public bool FarEastLineBreakControl { get; set; }
```

## Examples

Shows how to set special properties for Asian typography.

```csharp
Document doc = new Document(MyDir + "Document.docx");

ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.FarEastLineBreakControl = true;
format.WordWrap = false;
format.HangingPunctuation = true;

doc.Save(ArtifactsDir + "ParagraphFormat.AsianTypographyProperties.docx");
```

### See Also

* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
