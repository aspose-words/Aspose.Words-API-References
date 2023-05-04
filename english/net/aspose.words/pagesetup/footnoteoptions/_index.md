---
title: PageSetup.FootnoteOptions
linktitle: FootnoteOptions
articleTitle: FootnoteOptions
second_title: Aspose.Words for .NET
description: PageSetup FootnoteOptions property. Provides options that control numbering and positioning of footnotes in this section in C#.
type: docs
weight: 150
url: /net/aspose.words/pagesetup/footnoteoptions/
---
## PageSetup.FootnoteOptions property

Provides options that control numbering and positioning of footnotes in this section.

```csharp
public FootnoteOptions FootnoteOptions { get; }
```

## Examples

Shows how to configure options affecting footnotes/endnotes in a section.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote reference text.");

// Configure all footnotes in the first section to restart the numbering from 1
// at each new page and display themselves directly beneath the text on every page.
FootnoteOptions footnoteOptions = doc.Sections[0].PageSetup.FootnoteOptions;
footnoteOptions.Position = FootnotePosition.BeneathText;
footnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
footnoteOptions.StartNumber = 1;

builder.Write(" Hello again.");
builder.InsertFootnote(FootnoteType.Footnote, "Endnote reference text.");

// Configure all endnotes in the first section to maintain a continuous count throughout the section,
// starting from 1. Also, set them all to appear collected at the end of the document.
EndnoteOptions endnoteOptions = doc.Sections[0].PageSetup.EndnoteOptions;
endnoteOptions.Position = EndnotePosition.EndOfDocument;
endnoteOptions.RestartRule = FootnoteNumberingRule.Continuous;
endnoteOptions.StartNumber = 1;

doc.Save(ArtifactsDir + "PageSetup.FootnoteOptions.docx");
```

### See Also

* class [FootnoteOptions](../../../aspose.words.notes/footnoteoptions/)
* class [PageSetup](../)
* namespace [Aspose.Words](../../pagesetup/)
* assembly [Aspose.Words](../../../)
