---
title: Document.viewOptions property
linktitle: viewOptions property
articleTitle: viewOptions property
second_title: Aspose.Words for NodeJs
description: "Document.viewOptions property. Provides options to control how the document is displayed in Microsoft Word."
type: docs
weight: 470
url: /nodejs-net/Aspose.Words/document/viewOptions/
---

## Document.viewOptions property

Provides options to control how the document is displayed in Microsoft Word.


```js
get viewOptions(): Aspose.Words.Settings.ViewOptions
```

### Examples

Shows how to set a custom zoom factor, which older versions of Microsoft Word will apply to a document upon loading.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

doc.viewOptions.viewType = aw.Settings.ViewType.PageLayout;
doc.viewOptions.zoomPercent = 50;

expect(doc.viewOptions.zoomType).toEqual(aw.Settings.ZoomType.Custom);
expect(doc.viewOptions.zoomType).toEqual(aw.Settings.ZoomType.None);

doc.save(base.artifactsDir + "ViewOptions.SetZoomPercentage.doc");
```

Shows how to set a custom zoom type, which older versions of Microsoft Word will apply to a document upon loading.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
builder.writeln("Hello world!");

// Set the "ZoomType" property to "ZoomType.PageWidth" to get Microsoft Word
// to automatically zoom the document to fit the width of the page.
// Set the "ZoomType" property to "ZoomType.FullPage" to get Microsoft Word
// to automatically zoom the document to make the entire first page visible.
// Set the "ZoomType" property to "ZoomType.TextFit" to get Microsoft Word
// to automatically zoom the document to fit the inner text margins of the first page.
doc.viewOptions.zoomType = zoomType;

doc.save(base.artifactsDir + "ViewOptions.SetZoomType.doc");
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)

