---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: Aspose.Words for .NET
description: Discover how the ParagraphFormat WordWrap property affects text wrapping in Word. Learn to control Latin text flow for improved document readability.
type: docs
weight: 420
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
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
