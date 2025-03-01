---
title: DocumentBuilder.InsertFootnote
linktitle: InsertFootnote
articleTitle: InsertFootnote
second_title: Aspose.Words for .NET
description: Enhance your documents effortlessly with the DocumentBuilder InsertFootnote method—easily add footnotes or endnotes for better clarity and professionalism.
type: docs
weight: 340
url: /net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string*) {#insertfootnote}

Inserts a footnote or endnote into the document.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| Parameter | Type | Description |
| --- | --- | --- |
| footnoteType | FootnoteType | Specifies whether to insert a footnote or an endnote. |
| footnoteText | String | Specifies the text of the footnote. |

### Return Value

Returns a footnote object that was just created.

## Examples

Shows how to reference text with a footnote and an endnote.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert some text and mark it with a footnote with the IsAuto property set to "true" by default,
// so the marker seen in the body text will be auto-numbered at "1",
// and the footnote will appear at the bottom of the page.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Insert more text and mark it with an endnote with a custom reference mark,
// which will be used in place of the number "2" and set "IsAuto" to false.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Footnotes always appear at the bottom of their referenced text,
// so this page break will not affect the footnote.
// On the other hand, endnotes are always at the end of the document
// so that this page break will push the endnote down to the next page.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### See Also

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)

---

## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string, string*) {#insertfootnote_1}

Inserts a footnote or endnote into the document.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText, string referenceMark)
```

| Parameter | Type | Description |
| --- | --- | --- |
| footnoteType | FootnoteType | Specifies whether to insert a footnote or an endnote. |
| footnoteText | String | Specifies the text of the footnote. |
| referenceMark | String | Specifies the custom reference mark of the footnote. |

### Return Value

Returns a footnote object that was just created.

## Examples

Shows how to reference text with a footnote and an endnote.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert some text and mark it with a footnote with the IsAuto property set to "true" by default,
// so the marker seen in the body text will be auto-numbered at "1",
// and the footnote will appear at the bottom of the page.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Insert more text and mark it with an endnote with a custom reference mark,
// which will be used in place of the number "2" and set "IsAuto" to false.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Footnotes always appear at the bottom of their referenced text,
// so this page break will not affect the footnote.
// On the other hand, endnotes are always at the end of the document
// so that this page break will push the endnote down to the next page.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### See Also

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
