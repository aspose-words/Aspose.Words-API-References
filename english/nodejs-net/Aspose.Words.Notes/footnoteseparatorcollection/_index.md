---
title: FootnoteSeparatorCollection class
linktitle: FootnoteSeparatorCollection class
articleTitle: FootnoteSeparatorCollection class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Notes.FootnoteSeparatorCollection class. Provides typed access to [FootnoteSeparator](../footnoteseparator/) nodes of a document."
type: docs
weight: 80
url: /nodejs-net/aspose.words.notes/footnoteseparatorcollection/
---

## FootnoteSeparatorCollection class

Provides typed access to [FootnoteSeparator](../footnoteseparator/) nodes of a document.



### Constructors
| Name | Description |
| --- | --- |
| [FootnoteSeparatorCollection()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [this[]](./this[]/) |  |

### Examples

Shows how to manage footnote separator format.

```js
let doc = new aw.Document(base.myDir + "Footnotes and endnotes.docx");

let footnoteSeparator = doc.footnoteSeparators.at(aw.Notes.FootnoteSeparatorType.FootnoteSeparator);
// Align footnote separator.
footnoteSeparator.firstParagraph.paragraphFormat.alignment = aw.ParagraphAlignment.Center;
```

### See Also

* module [Aspose.Words.Notes](../)

