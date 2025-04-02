---
title: FindReplaceOptions.ignoreFootnotes property
linktitle: ignoreFootnotes property
articleTitle: ignoreFootnotes property
second_title: Aspose.Words for NodeJs
description: "FindReplaceOptions.ignoreFootnotes property. Gets or sets a boolean value indicating either to ignore footnotes"
type: docs
weight: 90
url: /nodejs-net/Aspose.Words.Replacing/findreplaceoptions/ignoreFootnotes/
---

## FindReplaceOptions.ignoreFootnotes property

Gets or sets a boolean value indicating either to ignore footnotes.
The default value is ``False``.



```js
get ignoreFootnotes(): boolean
```

### Examples

Shows how to ignore footnotes during a find-and-replace operation.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.insertFootnote(aw.Notes.FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.insertParagraph();

builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.insertFootnote(aw.Notes.FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Set the "IgnoreFootnotes" flag to "true" to get the find-and-replace
// operation to ignore text inside footnotes.
// Set the "IgnoreFootnotes" flag to "false" to get the find-and-replace
// operation to also search for text inside footnotes.
let options = new aw.Replacing.FindReplaceOptions();
options.ignoreFootnotes = isIgnoreFootnotes;
doc.range.replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### See Also

* module [Aspose.Words.Replacing](../../)
* class [FindReplaceOptions](../)

