---
title: PageSet class
linktitle: PageSet class
articleTitle: PageSet class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.PageSet class. Describes a random set of pages"
type: docs
weight: 570
url: /nodejs-net/aspose.words.saving/pageset/
---

## PageSet class

Describes a random set of pages.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/nodejs-net/programming-with-documents/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [PageSet(page)](./constructor/#number) | Creates an one-page set based on exact page index. |
| [PageSet(pages)](./constructor/#number[]) | Creates a page set based on exact page indices. |
| [PageSet(ranges)](./constructor/#pagerange[]) | Creates a page set based on ranges. |

### Properties

| Name | Description |
| --- | --- |
| [all](./all/) | Gets a set with all the pages of the document in their original order. |
| [even](./even/) | Gets a set with all the even pages of the document in their original order. |
| [odd](./odd/) | Gets a set with all the odd pages of the document in their original order. |

### Examples

Shows how to render one page from a document to a JPEG image.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.writeln("Page 1.");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 2.");
builder.insertImage(base.imageDir + "Logo.jpg");
builder.insertBreak(aw.BreakType.PageBreak);
builder.writeln("Page 3.");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
let options = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Jpeg);
// Set the "PageSet" to "1" to select the second page via
// the zero-based index to start rendering the document from.
options.pageSet = new aw.Saving.PageSet(1);

// When we save the document to the JPEG format, Aspose.words only renders one page.
// This image will contain one page starting from page two,
// which will just be the second page of the original document.
doc.save(base.artifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### See Also

* module [Aspose.Words.Saving](../)

