---
title: HtmlFixedSaveOptions.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for NodeJs
description: "HtmlFixedSaveOptions.encoding property. Specifies the encoding to use when exporting to HTML"
type: docs
weight: 30
url: /nodejs-net/Aspose.Words.Saving/htmlfixedsaveoptions/encoding/
---

## HtmlFixedSaveOptions.encoding property

Specifies the encoding to use when exporting to HTML.
Default value is ``new UTF8Encoding(true)`` (UTF-8 with BOM).



```js
get encoding(): string
```

### Examples

Shows how to set which encoding to use while exporting a document to HTML.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Hello World!");

// The default encoding is UTF-8. If we want to represent our document using a different encoding,
// we can use a SaveOptions object to set a specific encoding.
let htmlFixedSaveOptions = new aw.Saving.HtmlFixedSaveOptions();
htmlFixedSaveOptions.encoding = "ascii";

expect(htmlFixedSaveOptions.encoding).toEqual("US-ASCII");

doc.save(base.artifactsDir + "HtmlFixedSaveOptions.UseEncoding.html", htmlFixedSaveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [HtmlFixedSaveOptions](../)

