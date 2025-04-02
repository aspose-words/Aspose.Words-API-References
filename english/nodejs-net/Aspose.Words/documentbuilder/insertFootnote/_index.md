---
title: DocumentBuilder.insertFootnote method
linktitle: insertFootnote method
articleTitle: insertFootnote method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentBuilder.insertFootnote method"
type: docs
weight: 340
url: /nodejs-net/Aspose.Words/documentbuilder/insertFootnote/
---

## insertFootnote(footnoteType, footnoteText) {#footnotetype_string}

Inserts a footnote or endnote into the document.


```js
insertFootnote(footnoteType: Aspose.Words.Notes.FootnoteTypefootnoteText: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| footnoteType | [FootnoteType](../../../Aspose.Words.Notes/footnotetype/) | Specifies whether to insert a footnote or an endnote. |
| footnoteText | string | Specifies the text of the footnote. |

### Returns

Returns a footnote object that was just created.


## insertFootnote(footnoteType, footnoteText, referenceMark) {#footnotetype_string_string}

Inserts a footnote or endnote into the document.


```js
insertFootnote(footnoteType: Aspose.Words.Notes.FootnoteTypefootnoteText: stringreferenceMark: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| footnoteType | [FootnoteType](../../../Aspose.Words.Notes/footnotetype/) | Specifies whether to insert a footnote or an endnote. |
| footnoteText | string | Specifies the text of the footnote. |
| referenceMark | string | Specifies the custom reference mark of the footnote. |

### Returns

Returns a footnote object that was just created.


## Examples

Shows how to reference text with a footnote and an endnote.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert some text and mark it with a footnote with the IsAuto property set to "true" by default,
// so the marker seen in the body text will be auto-numbered at "1",
// and the footnote will appear at the bottom of the page.
builder.write("This text will be referenced by a footnote.");
builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Insert more text and mark it with an endnote with a custom reference mark,
// which will be used in place of the number "2" and set "IsAuto" to false.
builder.write("This text will be referenced by an endnote.");
builder.insertFootnote(aw.Notes.FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Footnotes always appear at the bottom of their referenced text,
// so this page break will not affect the footnote.
// On the other hand, endnotes are always at the end of the document
// so that this page break will push the endnote down to the next page.
builder.insertBreak(aw.BreakType.PageBreak);

doc.save(base.artifactsDir + "DocumentBuilder.insertFootnote.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

