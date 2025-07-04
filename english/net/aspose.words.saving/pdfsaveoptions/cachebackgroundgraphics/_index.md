---
title: PdfSaveOptions.CacheBackgroundGraphics
linktitle: CacheBackgroundGraphics
articleTitle: CacheBackgroundGraphics
second_title: Aspose.Words for .NET
description: Discover the PdfSaveOptions CacheBackgroundGraphics property to optimize document graphics caching, enhancing your PDF creation and performance.
type: docs
weight: 40
url: /net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

Gets or sets a value determining whether or not to cache graphics placed in document's background.

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

## Remarks

Default value is `true` and background graphics are written to the PDF document as an xObject.

When the value is `false` background graphics are not cached.

Some shapes are not supported for caching(shapes with fields, bookmarks, HRefs).

Document background graphic is various shapes, charts, images placed in the footer or header, well as background and border of a page.

## Examples

Shows how to cache graphics placed in document's background.

```csharp
Document doc = new Document(MyDir + "Background images.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.CacheBackgroundGraphics = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf", saveOptions);

long asposeToPdfSize = new FileInfo(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf").Length;
long wordToPdfSize = new FileInfo(MyDir + "Background images (word to pdf).pdf").Length;

Assert.That(asposeToPdfSize, Is.LessThan(wordToPdfSize));
```

### See Also

* class [PdfSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
