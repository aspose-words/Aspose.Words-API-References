---
title: PageRange Class
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Saving.PageRange class for defining continuous page ranges easily. Enhance your document processing with precision and efficiency.
type: docs
weight: 6000
url: /net/aspose.words.saving/pagerange/
---
## PageRange class

Represents a continuous range of pages.

To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/net/programming-with-documents/) documentation article.

```csharp
public sealed class PageRange
```

## Constructors

| Name | Description |
| --- | --- |
| [PageRange](pagerange/)(*int, int*) | Creates a new page range object. |

## Examples

Shows how to extract pages based on exact page ranges.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
