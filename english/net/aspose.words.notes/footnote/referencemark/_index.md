---
title: Footnote.ReferenceMark
second_title: Aspose.Words for .NET API Reference
description: Footnote property. Gets/sets custom reference mark to be used for this footnote. Default value is empty string Empty meaning autonumbered footnotes are used in C#.
type: docs
weight: 50
url: /net/aspose.words.notes/footnote/referencemark/
---
## Footnote.ReferenceMark property

Gets/sets custom reference mark to be used for this footnote. Default value is **empty string** (Empty), meaning auto-numbered footnotes are used.

```csharp
public string ReferenceMark { get; set; }
```

## Remarks

If this property is set to **empty string** (Empty) or `null`, then [`IsAuto`](../isauto/) property will automatically be set to `true`, if set to anything else then [`IsAuto`](../isauto/) will be set to `false`.

RTF-format can only store 1 symbol as custom reference mark, so upon export only the first symbol will be written others will be discard.

## Examples

Shows how to insert and customize footnotes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Add text, and reference it with a footnote. This footnote will place a small superscript reference
// mark after the text that it references and create an entry below the main body text at the bottom of the page.
// This entry will contain the footnote's reference mark and the reference text,
// which we will pass to the document builder's "InsertFootnote" method.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// If this property is set to "true", then our footnote's reference mark
// will be its index among all the section's footnotes.
// This is the first footnote, so the reference mark will be "1".
Assert.True(footnote.IsAuto);

// We can move the document builder inside the footnote to edit its reference text. 
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// We can set a custom reference mark which the footnote will use instead of its index number.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// A bookmark with the "IsAuto" flag set to true will still show its real index
// even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### See Also

* class [Footnote](../)
* namespace [Aspose.Words.Notes](../../footnote/)
* assembly [Aspose.Words](../../../)
