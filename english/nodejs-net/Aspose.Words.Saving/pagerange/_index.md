---
title: PageRange class
linktitle: PageRange class
articleTitle: PageRange class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Saving.PageRange class. Represents a continuous range of pages"
type: docs
weight: 560
url: /nodejs-net/aspose.words.saving/pagerange/
---

## PageRange class

Represents a continuous range of pages.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/nodejs-net/programming-with-documents/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [PageRange(from, to)](./constructor/#number_number) | Creates a new page range object. |

### Examples

Shows how to extract pages based on exact page ranges.

```js
let doc = new aw.Document(base.myDir + "Images.docx");

let imageOptions = new aw.Saving.ImageSaveOptions(aw.SaveFormat.Tiff);
let pageSet = new aw.Saving.PageSet(new aw.Saving.PageRange(1, 1), new aw.Saving.PageRange(2, 3), new aw.Saving.PageRange(1, 3),
  new aw.Saving.PageRange(2, 4), new aw.Saving.PageRange(1, 1));

imageOptions.pageSet = pageSet;
doc.save(base.artifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### See Also

* module [Aspose.Words.Saving](../)

