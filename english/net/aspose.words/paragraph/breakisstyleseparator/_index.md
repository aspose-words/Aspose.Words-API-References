---
title: BreakIsStyleSeparator
second_title: Aspose.Words for .NET API Reference
description: Paragraph property. True if this paragraph break is a Style Separator. A style separator allows one paragraph to consist of parts that have different paragraph styles in C#.
type: docs
weight: 20
url: /net/aspose.words/paragraph/breakisstyleseparator/
---
## Paragraph.BreakIsStyleSeparator property

True if this paragraph break is a Style Separator. A style separator allows one paragraph to consist of parts that have different paragraph styles.

```csharp
public bool BreakIsStyleSeparator { get; }
```

## Examples

Shows how to write text to the same line as a TOC heading and have it not show up in the TOC.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertTableOfContents("\\o \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Insert a paragraph with a style that the TOC will pick up as an entry.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

// Both these strings are in the same paragraph and will therefore show up on the same TOC entry.
builder.Write("Heading 1. ");
builder.Write("Will appear in the TOC. ");

// If we insert a style separator, we can write more text in the same paragraph
// and use a different style without showing up in the TOC.
// If we use a heading type style after the separator, we can draw multiple TOC entries from one document text line.
builder.InsertStyleSeparator();
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Quote;
builder.Write("Won't appear in the TOC. ");

Assert.True(doc.FirstSection.Body.FirstParagraph.BreakIsStyleSeparator);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Paragraph.BreakIsStyleSeparator.docx");
```

### See Also

* class [Paragraph](../)
* namespace [Aspose.Words](../../paragraph/)
* assembly [Aspose.Words](../../../)
