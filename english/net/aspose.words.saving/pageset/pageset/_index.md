---
title: PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words for .NET
description: PageSet constructor. Creates an onepage set based on exact page index in C#.
type: docs
weight: 10
url: /net/aspose.words.saving/pageset/pageset/
---
## PageSet(*int*) {#constructor_1}

Creates an one-page set based on exact page index.

```csharp
public PageSet(int page)
```

| Parameter | Type | Description |
| --- | --- | --- |
| page | Int32 | Zero-based index of the page. |

## Remarks

If a page is encountered that is not in the document, an exception will be thrown during rendering. MaxValue means the last page in the document.

### See Also

* class [PageSet](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)

---

## PageSet(*params int[]*) {#constructor_2}

Creates a page set based on exact page indices.

```csharp
public PageSet(params int[] pages)
```

| Parameter | Type | Description |
| --- | --- | --- |
| pages | Int32[] | Zero-based indices of pages. |

## Remarks

If a page is encountered that is not in the document, an exception will be thrown during rendering. MaxValue means the last page in the document.

## Examples

Shows how to extract pages based on exact page indices.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Add five pages to the document.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Create an "XpsSaveOptions" object, which we can pass to the document's "Save" method
// to modify how that method converts the document to .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Use the "PageSet" property to select a set of the document's pages to save to output XPS.
// In this case, we will choose, via a zero-based index, only three pages: page 1, page 2, and page 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### See Also

* class [PageSet](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)

---

## PageSet(*params PageRange[]*) {#constructor}

Creates a page set based on ranges.

```csharp
public PageSet(params PageRange[] ranges)
```

| Parameter | Type | Description |
| --- | --- | --- |
| ranges | PageRange[] | Array of page ranges. |

## Remarks

If a range is encountered that starts after the last page in the document, an exception will be thrown during rendering. All ranges that end after the last page are truncated to fit in the document.

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

* class [PageRange](../../pagerange/)
* class [PageSet](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
