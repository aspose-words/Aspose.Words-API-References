---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
linktitle: IncludeTextboxesFootnotesEndnotesInStat
articleTitle: IncludeTextboxesFootnotesEndnotesInStat
second_title: Aspose.Words for .NET
description: Document IncludeTextboxesFootnotesEndnotesInStat property. Specifies whether to include textboxes footnotes and endnotes in word count statistics in C#.
type: docs
weight: 220
url: /net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

Specifies whether to include textboxes, footnotes and endnotes in word count statistics.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

## Examples

Shows how to include or exclude textboxes, footnotes and endnotes from word count statistics.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

// By default option is set to 'false'.
doc.UpdateWordCount();
// Words count without textboxes, footnotes and endnotes.
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Words);            

doc.IncludeTextboxesFootnotesEndnotesInStat = true;
doc.UpdateWordCount();
// Words count with textboxes, footnotes and endnotes.
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### See Also

* class [Document](../)
* namespace [Aspose.Words](../../document/)
* assembly [Aspose.Words](../../../)
