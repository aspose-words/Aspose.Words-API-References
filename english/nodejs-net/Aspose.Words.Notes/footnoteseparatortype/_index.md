---
title: FootnoteSeparatorType enumeration
linktitle: FootnoteSeparatorType enumeration
articleTitle: FootnoteSeparatorType enumeration
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Notes.FootnoteSeparatorType enumeration. Specifies the type of the footnote/endnote separator."
type: docs
weight: 90
url: /nodejs-net/aspose.words.notes/footnoteseparatortype/
---

## FootnoteSeparatorType enumeration

Specifies the type of the footnote/endnote separator.


### Members

| Name | Description |
| --- | --- |
| FootnoteSeparator | Separator between main text and footnote text. |
| FootnoteContinuationSeparator | Printed above footnote text on a page when the text must be continued from a previous page. |
| FootnoteContinuationNotice | Printed below footnote text on a page when footnote text must be continued on a succeeding page. |
| EndnoteSeparator | Separator between main text and endnote text. |
| EndnoteContinuationSeparator | Printed above endnote text on a page when the text must be continued from a previous page. |
| EndnoteContinuationNotice | Printed below endnote text on a page when endnote text must be continued on a succeeding page. |

### Examples

Shows how to remove endnote separator.

```js
let doc = new aw.Document(base.myDir + "Footnotes and endnotes.docx");

let endnoteSeparator = doc.footnoteSeparators.at(aw.Notes.FootnoteSeparatorType.EndnoteSeparator);
// Remove endnote separator.
endnoteSeparator.firstParagraph.firstChild.remove();
```

Shows how to manage footnote separator format.

```js
let doc = new aw.Document(base.myDir + "Footnotes and endnotes.docx");

let footnoteSeparator = doc.footnoteSeparators.at(aw.Notes.FootnoteSeparatorType.FootnoteSeparator);
// Align footnote separator.
footnoteSeparator.firstParagraph.paragraphFormat.alignment = aw.ParagraphAlignment.Center;
```

### See Also

* module [Aspose.Words.Notes](../)

