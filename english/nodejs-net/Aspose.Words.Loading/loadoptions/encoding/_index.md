---
title: LoadOptions.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for NodeJs
description: "LoadOptions.encoding property. Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified inside the document"
type: docs
weight: 50
url: /nodejs-net/aspose.words.loading/loadoptions/encoding/
---

## LoadOptions.encoding property

Gets or sets the encoding that will be used to load an HTML, TXT, or CHM document if the encoding is not specified
inside the document.
Can be ``null``. Default is ``null``.



```js
get encoding(): string
```

### Remarks

This property is used only when loading HTML, TXT, or CHM documents.

If encoding is not specified inside the document and this property is ``null``, then the system will try to
automatically detect the encoding.




### Examples

Shows how to set the encoding with which to open a document.

```js
let loadOptions = new aw.Loading.LoadOptions();
loadOptions.encoding = "ascii";

// Load the document while passing the LoadOptions object, then verify the document's contents.
let doc = new aw.Document(base.myDir + "English text.txt", loadOptions);

expect(doc.toString(aw.SaveFormat.Text).includes("This is a sample text in English.")).toEqual(true);
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [LoadOptions](../)

