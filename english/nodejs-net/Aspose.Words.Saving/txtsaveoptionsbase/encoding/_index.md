---
title: TxtSaveOptionsBase.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for Node.js
description: "TxtSaveOptionsBase.encoding property. Specifies the encoding to use when exporting in text formats"
type: docs
weight: 10
url: /nodejs-net/aspose.words.saving/txtsaveoptionsbase/encoding/
---

## TxtSaveOptionsBase.encoding property

Specifies the encoding to use when exporting in text formats. 
Default value is .


```js
get encoding(): string
```

### Examples

Shows how to set encoding for a .txt output document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Add some text with characters from outside the ASCII character set.
builder.write("À È Ì Ò Ù.");

// Create a "TxtSaveOptions" object, which we can pass to the document's "Save" method
// to modify how we save the document to plaintext.
let txtSaveOptions = new aw.Saving.TxtSaveOptions();

// Verify that the "Encoding" property contains the appropriate encoding for our document's contents.
expect(txtSaveOptions.encoding).toEqual("utf-8");

doc.save(base.artifactsDir + "TxtSaveOptions.encoding.UTF8.txt", txtSaveOptions);

let docText = readTextFile(base.artifactsDir + "TxtSaveOptions.encoding.UTF8.txt", false, "utf8");

expect(docText).toEqual("\uFEFFÀ È Ì Ò Ù.\r\n");

// Using an unsuitable encoding may result in a loss of document contents.
txtSaveOptions.encoding = "us-ascii";
doc.save(base.artifactsDir + "TxtSaveOptions.encoding.ASCII.txt", txtSaveOptions);
docText = readTextFile(base.artifactsDir + "TxtSaveOptions.encoding.ASCII.txt", false, "ascii");

expect(docText).toEqual("? ? ? ? ?.\r\n");
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [TxtSaveOptionsBase](../)

