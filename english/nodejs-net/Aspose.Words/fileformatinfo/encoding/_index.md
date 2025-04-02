---
title: FileFormatInfo.encoding property
linktitle: encoding property
articleTitle: encoding property
second_title: Aspose.Words for NodeJs
description: "FileFormatInfo.encoding property. Gets the detected encoding if applicable to the current document format"
type: docs
weight: 10
url: /nodejs-net/Aspose.Words/fileformatinfo/encoding/
---

## FileFormatInfo.encoding property

Gets the detected encoding if applicable to the current document format.
At the moment detects encoding only for HTML documents.


```js
get encoding(): string
```

### Examples

Shows how to detect encoding in an html file.

```js
let info = aw.FileFormatUtil.detectFileFormat(base.myDir + "Document.html");

expect(info.loadFormat).toEqual(aw.LoadFormat.Html);

// The Encoding property is used only when we create a FileFormatInfo object for an html document.
expect(info.encoding).toEqual("windows-1252");
```

### See Also

* module [Aspose.Words](../../)
* class [FileFormatInfo](../)

