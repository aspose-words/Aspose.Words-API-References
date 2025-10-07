---
title: PdfSaveOptions.preblendImages property
linktitle: preblendImages property
articleTitle: preblendImages property
second_title: Aspose.Words for Node.js
description: "PdfSaveOptions.preblendImages property. Gets or sets a value determining whether or not to preblend transparent images with black background color."
type: docs
weight: 280
url: /nodejs-net/aspose.words.saving/pdfsaveoptions/preblendImages/
---

## PdfSaveOptions.preblendImages property

Gets or sets a value determining whether or not to preblend transparent images with black background color.


```js
get preblendImages(): boolean
```

### Remarks

Preblending images may improve PDF document visual appearance in Adobe Reader and remove anti-aliasing artifacts.

In order to properly display preblended images, PDF viewer application must support /Matte entry in soft-mask image dictionary.
Also preblending images may decrease PDF rendering performance.

The default value is ``false``.




### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

