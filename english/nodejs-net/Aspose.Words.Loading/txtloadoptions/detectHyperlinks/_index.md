---
title: TxtLoadOptions.detectHyperlinks property
linktitle: detectHyperlinks property
articleTitle: detectHyperlinks property
second_title: Aspose.Words for NodeJs
description: "TxtLoadOptions.detectHyperlinks property. Specifies either to detect hyperlinks in text"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Loading/txtloadoptions/detectHyperlinks/
---

## TxtLoadOptions.detectHyperlinks property

Specifies either to detect hyperlinks in text.
The default value is ``False``.



```js
get detectHyperlinks(): boolean
```

### Examples

Shows how to read and display hyperlinks.

```js
const inputText = "Some links in TXT:\n" +
    "https://www.aspose.com/\n" +
    "https://docs.aspose.com/words/net/\n";

// Load document with hyperlinks.
let loadOptions = new aw.Loading.TxtLoadOptions();
loadOptions.detectHyperlinks = true;
let doc = new aw.Document(Buffer.from(inputText), loadOptions);

// Print hyperlinks text.
for (let field of doc.range.fields)
  console.log(field.result);

expect(doc.range.fields.at(0).result.trim()).toEqual("https://www.aspose.com/");
expect(doc.range.fields.at(1).result.trim()).toEqual("https://docs.aspose.com/words/net/");
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [TxtLoadOptions](../)

