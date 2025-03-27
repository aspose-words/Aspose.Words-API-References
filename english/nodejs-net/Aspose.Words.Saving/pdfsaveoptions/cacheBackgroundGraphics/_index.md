---
title: PdfSaveOptions.cacheBackgroundGraphics property
linktitle: cacheBackgroundGraphics property
articleTitle: cacheBackgroundGraphics property
second_title: Aspose.Words for NodeJs
description: "PdfSaveOptions.cacheBackgroundGraphics property. Gets or sets a value determining whether or not to cache graphics placed in document's background."
type: docs
weight: 40
url: /nodejs-net/Aspose.Words.Saving/pdfsaveoptions/cacheBackgroundGraphics/
---

## PdfSaveOptions.cacheBackgroundGraphics property

Gets or sets a value determining whether or not to cache graphics placed in document's background.


```js
get cacheBackgroundGraphics(): boolean
```

### Remarks

Default value is ``True`` and background graphics are written to the PDF document as an xObject.

When the value is ``False`` background graphics are not cached.

Some shapes are not supported for caching(shapes with fields, bookmarks, HRefs).

Document background graphic is various shapes, charts, images placed in the footer or header,
well as background and border of a page.




### Examples

Shows how to cache graphics placed in document's background.

```js
let doc = new aw.Document(base.myDir + "Background images.docx");

let saveOptions = new aw.Saving.PdfSaveOptions();
saveOptions.cacheBackgroundGraphics = true;

doc.save(base.artifactsDir + "PdfSaveOptions.cacheBackgroundGraphics.pdf", saveOptions);

let asposeToPdfSize = fs.statSync(base.artifactsDir + "PdfSaveOptions.cacheBackgroundGraphics.pdf").size;
let wordToPdfSize = fs.statSync(base.myDir + "Background images (word to pdf).pdf").size;

expect(asposeToPdfSize <= wordToPdfSize).toBe(true);
```

### See Also

* module [Aspose.Words.Saving](../../)
* class [PdfSaveOptions](../)

