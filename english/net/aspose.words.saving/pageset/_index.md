---
title: PageSet Class
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Saving.PageSet class for efficient document management. Easily define random page sets and enhance your workflow today!
type: docs
weight: 6170
url: /net/aspose.words.saving/pageset/
---
## PageSet class

Describes a random set of pages.

To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/net/programming-with-documents/) documentation article.

```csharp
public sealed class PageSet : IEnumerable<int>
```

## Constructors

| Name | Description |
| --- | --- |
| [PageSet](pageset/#constructor_1)(*int*) | Creates an one-page set based on exact page index. |
| [PageSet](pageset/#constructor_2)(*params int[]*) | Creates a page set based on exact page indices. |
| [PageSet](pageset/#constructor)(*params PageRange[]*) | Creates a page set based on ranges. |

## Properties

| Name | Description |
| --- | --- |
| static [All](../../aspose.words.saving/pageset/all/) { get; } | Gets a set with all the pages of the document in their original order. |
| static [Even](../../aspose.words.saving/pageset/even/) { get; } | Gets a set with all the even pages of the document in their original order. |
| static [Odd](../../aspose.words.saving/pageset/odd/) { get; } | Gets a set with all the odd pages of the document in their original order. |

## Methods

| Name | Description |
| --- | --- |
| [GetEnumerator](../../aspose.words.saving/pageset/getenumerator/)() |  |

## Examples

Shows how to render one page from a document to a JPEG image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
// to modify the way in which that method renders the document into an image.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// Set the "PageSet" to "1" to select the second page via
// the zero-based index to start rendering the document from.
options.PageSet = new PageSet(1);

// When we save the document to the JPEG format, Aspose.Words only renders one page.
// This image will contain one page starting from page two,
// which will just be the second page of the original document.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
