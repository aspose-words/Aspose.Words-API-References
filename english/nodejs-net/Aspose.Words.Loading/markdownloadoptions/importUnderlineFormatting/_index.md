---
title: MarkdownLoadOptions.importUnderlineFormatting property
linktitle: importUnderlineFormatting property
articleTitle: importUnderlineFormatting property
second_title: Aspose.Words for Node.js
description: "MarkdownLoadOptions.importUnderlineFormatting property. Gets or sets a boolean value indicating either to recognize a sequence of two plus characters ++ as underline text formatting"
type: docs
weight: 20
url: /nodejs-net/aspose.words.loading/markdownloadoptions/importUnderlineFormatting/
---

## MarkdownLoadOptions.importUnderlineFormatting property

Gets or sets a boolean value indicating either to recognize a sequence
of two plus characters "++" as underline text formatting.
The default value is ``false``.



```js
get importUnderlineFormatting(): boolean
```

### Examples

Shows how to recognize plus characters "++" as underline text formatting.

```js
using (MemoryStream stream = new MemoryStream(Encoding.ASCII.GetBytes("++12 and B++")))
{
  let loadOptions = new aw.Loading.MarkdownLoadOptions() { ImportUnderlineFormatting = true };
  let doc = new aw.Document(stream, loadOptions);

  let para = (Paragraph)doc.getChild(aw.NodeType.Paragraph, 0, true);
  expect(para.runs.at(0).font.underline).toEqual(aw.Underline.Single);

  loadOptions = new aw.Loading.MarkdownLoadOptions() { ImportUnderlineFormatting = false };
  doc = new aw.Document(stream, loadOptions);

  para = (Paragraph)doc.getChild(aw.NodeType.Paragraph, 0, true);
  expect(para.runs.at(0).font.underline).toEqual(aw.Underline.None);
}
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [MarkdownLoadOptions](../)

