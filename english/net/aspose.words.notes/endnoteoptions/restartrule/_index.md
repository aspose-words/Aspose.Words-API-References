---
title: EndnoteOptions.RestartRule
linktitle: RestartRule
articleTitle: RestartRule
second_title: Aspose.Words for .NET
description: Discover how the EndnoteOptions RestartRule property enhances your document by controlling automatic numbering for a polished, professional look.
type: docs
weight: 30
url: /net/aspose.words.notes/endnoteoptions/restartrule/
---
## EndnoteOptions.RestartRule property

Determines when automatic numbering restarts.

```csharp
public FootnoteNumberingRule RestartRule { get; set; }
```

## Remarks

Not all values are applicable to endnotes. To ascertain which values are applicable see [`FootnoteNumberingRule`](../../footnotenumberingrule/).

## Examples

Shows how to restart footnote/endnote numbering at certain places in the document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Footnotes and endnotes are a way to attach a reference or a side comment to text
// that does not interfere with the main body text's flow. 
// Inserting a footnote/endnote adds a small superscript reference symbol
// at the main body text where we insert the footnote/endnote.
// Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
// symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
// Footnote entries, by default, show up at the bottom of each page that contains
// their reference symbols, and endnotes show up at the end of the document.
builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote 4.");

builder.InsertBreak(BreakType.PageBreak);

builder.Write("Text 1. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 1.");
builder.Write("Text 2. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 2.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Text 3. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 3.");
builder.Write("Text 4. ");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote 4.");

// By default, the reference symbol for each footnote and endnote is its index
// among all the document's footnotes/endnotes. Each document maintains separate counts
// for footnotes and endnotes and does not restart these counts at any point.
Assert.That(FootnoteNumberingRule.Default, Is.EqualTo(doc.FootnoteOptions.RestartRule));
Assert.That(FootnoteNumberingRule.Continuous, Is.EqualTo(FootnoteNumberingRule.Default));

// We can use the "RestartRule" property to get the document to restart
// the footnote/endnote counts at a new page or section.
doc.FootnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
doc.EndnoteOptions.RestartRule = FootnoteNumberingRule.RestartSection;

doc.Save(ArtifactsDir + "InlineStory.NumberingRule.docx");
```

### See Also

* enum [FootnoteNumberingRule](../../footnotenumberingrule/)
* class [EndnoteOptions](../)
* namespace [Aspose.Words.Notes](../../../aspose.words.notes/)
* assembly [Aspose.Words](../../../)
