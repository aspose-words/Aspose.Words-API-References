---
title: DocumentBase.footnoteSeparators property
linktitle: footnoteSeparators property
articleTitle: footnoteSeparators property
second_title: Aspose.Words for Node.js
description: "DocumentBase.footnoteSeparators property. Provides access to the footnote/endnote separators defined in the document."
type: docs
weight: 40
url: /nodejs-net/aspose.words/documentbase/footnoteSeparators/
---

## DocumentBase.footnoteSeparators property

Provides access to the footnote/endnote separators defined in the document.


```js
get footnoteSeparators(): Aspose.Words.Notes.FootnoteSeparatorCollection
```

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

* module [Aspose.Words](../../)
* class [DocumentBase](../)

