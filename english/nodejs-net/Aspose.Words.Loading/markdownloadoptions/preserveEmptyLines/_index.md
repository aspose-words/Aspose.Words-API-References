---
title: MarkdownLoadOptions.preserveEmptyLines property
linktitle: preserveEmptyLines property
articleTitle: preserveEmptyLines property
second_title: Aspose.Words for NodeJs
description: "MarkdownLoadOptions.preserveEmptyLines property. Gets or sets a boolean value indicating whether to preserve empty lines while load a [LoadFormat.Markdown](../../../aspose.words/loadformat/#Markdown) document"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Loading/markdownloadoptions/preserveEmptyLines/
---

## MarkdownLoadOptions.preserveEmptyLines property

Gets or sets a boolean value indicating whether to preserve empty lines while load a [LoadFormat.Markdown](../../../aspose.words/loadformat/#Markdown) document.
The default value is ``False``.
Normally, empty lines between block-level elements in Markdown are ignored. Empty lines at the beginning and
end of the document are also ignored. This option allows to import such empty lines.




```js
get preserveEmptyLines(): boolean
```

### Examples

Shows how to preserve empty line while load a document.

```js
string mdText = `${Environment.NewLine}Line1${Environment.NewLine}${Environment.NewLine}Line2${Environment.NewLine}${Environment.NewLine}`;
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
  let loadOptions = new aw.Loading.MarkdownLoadOptions() { PreserveEmptyLines = true };
  let doc = new aw.Document(stream, loadOptions);

  expect(doc.getText()).toEqual("\rLine1\r\rLine2\r\f");
}
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [MarkdownLoadOptions](../)

