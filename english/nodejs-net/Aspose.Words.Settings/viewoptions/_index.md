---
title: ViewOptions class
linktitle: ViewOptions class
articleTitle: ViewOptions class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Settings.ViewOptions class. Provides various options that control how a document is shown in Microsoft Word"
type: docs
weight: 190
url: /nodejs-net/aspose.words.settings/viewoptions/
---

## ViewOptions class

Provides various options that control how a document is shown in Microsoft Word.
To learn more, visit the [Work with Options and Appearance of Word Documents](https://docs.aspose.com/words/nodejs-net/work-with-word-document-options-and-appearance/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [displayBackgroundShape](./displayBackgroundShape/) | Controls display of the background shape in print layout view. |
| [doNotDisplayPageBoundaries](./doNotDisplayPageBoundaries/) | Turns off display of the space between the top of the text and the top edge of the page. |
| [formsDesign](./formsDesign/) | Specifies whether the document is in forms design mode. |
| [viewType](./viewType/) | Controls the view mode in Microsoft Word. |
| [zoomPercent](./zoomPercent/) | Gets or sets the percentage (between 10 and 500) at which you want to view your document. |
| [zoomType](./zoomType/) | Gets or sets a zoom value based on the size of the window. |

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

* module [Aspose.Words.Settings](../)
* class [Document](../../aspose.words/document/)
* property [Document.viewOptions](../../aspose.words/document/viewOptions/)

