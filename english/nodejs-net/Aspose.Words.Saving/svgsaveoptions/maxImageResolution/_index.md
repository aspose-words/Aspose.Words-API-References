---
title: SvgSaveOptions.maxImageResolution property
linktitle: maxImageResolution property
articleTitle: maxImageResolution property
second_title: Aspose.Words for Node.js
description: "SvgSaveOptions.maxImageResolution property. Gets or sets a value in pixels per inch that limits resolution of exported raster images"
type: docs
weight: 50
url: /nodejs-net/aspose.words.saving/svgsaveoptions/maxImageResolution/
---

## SvgSaveOptions.maxImageResolution property

Gets or sets a value in pixels per inch that limits resolution of exported raster images. Default value is zero.


```js
get maxImageResolution(): number
```

### Remarks

If the value of this property is non-zero, it limits resolution of exported raster images.
That is, higher-resolution images are resampled down to the limit and lower-resolution images are exported as is.

If the value of this property is zero, all raster images are exported without resampling.




### Examples

Shows how to set limit for image resolution.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let saveOptions = new aw.Saving.SvgSaveOptions();
saveOptions.maxImageResolution = 72;

doc.save(base.artifactsDir + "SvgSaveOptions.maxImageResolution.svg", saveOptions);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [SvgSaveOptions](../)

