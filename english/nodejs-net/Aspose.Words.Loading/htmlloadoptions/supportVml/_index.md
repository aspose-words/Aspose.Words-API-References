---
title: HtmlLoadOptions.supportVml property
linktitle: supportVml property
articleTitle: supportVml property
second_title: Aspose.Words for NodeJs
description: "HtmlLoadOptions.supportVml property. Gets or sets a value indicating whether to support VML images."
type: docs
weight: 70
url: /nodejs-net/Aspose.Words.Loading/htmlloadoptions/supportVml/
---

## HtmlLoadOptions.supportVml property

Gets or sets a value indicating whether to support VML images.


```js
get supportVml(): boolean
```

### Examples

Shows how to support conditional comments while loading an HTML document.

```js
let loadOptions = new aw.Loading.HtmlLoadOptions();

// If the value is true, then we take VML code into account while parsing the loaded document.
loadOptions.supportVml = supportVml;

// This document contains a JPEG image within "<!--[if gte vml 1]>" tags,
// and a different PNG image within "<![if !vml]>" tags.
// If we set the "SupportVml" flag to "true", then Aspose.words will load the JPEG.
// If we set this flag to "false", then Aspose.words will only load the PNG.
let doc = new aw.Document(base.myDir + "VML conditional.htm", loadOptions);

if (supportVml)
  expect(doc.getShape(0, true).imageData.imageType).toEqual(aw.Drawing.ImageType.Jpeg);
else
  expect(doc.getShape(0, true).imageData.imageType).toEqual(aw.Drawing.ImageType.Png);
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [HtmlLoadOptions](../)

