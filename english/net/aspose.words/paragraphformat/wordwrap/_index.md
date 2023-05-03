---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: Aspose.Words for .NET API Reference
description: ParagraphFormat WordWrap property. If this property is false Latin text in the middle of a word can be wrapped for the current paragraph. Otherwise Latin text is wrapped by whole words in C#.
type: docs
weight: 400
url: /net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

If this property is `false`, Latin text in the middle of a word can be wrapped for the current paragraph. Otherwise Latin text is wrapped by whole words.

```csharp
public bool WordWrap { get; set; }
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
* namespace [Aspose.Words](../../paragraphformat/)
* assembly [Aspose.Words](../../../)
