---
title: ParagraphFormat.MirrorIndents
linktitle: MirrorIndents
articleTitle: MirrorIndents
second_title: Aspose.Words for .NET
description: Discover how the ParagraphFormat MirrorIndents property enhances your document formatting by ensuring consistent left and right indents for a polished look.
type: docs
weight: 240
url: /net/aspose.words/paragraphformat/mirrorindents/
---
## ParagraphFormat.MirrorIndents property

Gets or sets a flag indicating whether the left and right indents are of the same width.

```csharp
public bool MirrorIndents { get; set; }
```

## Examples

Show how to make left and right indents the same.

```csharp
Document doc = new Document(MyDir + "Document.docx");
ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;

format.MirrorIndents = true;

doc.Save(ArtifactsDir + "ParagraphFormat.MirrorIndents.docx");
```

### See Also

* class [ParagraphFormat](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
