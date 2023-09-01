---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
linktitle: EmulateRenderingToSizeOnPage
articleTitle: EmulateRenderingToSizeOnPage
second_title: Aspose.Words for .NET
description: MetafileRenderingOptions EmulateRenderingToSizeOnPage property. Gets or sets a value determining whether metafile rendering emulates the display of the metafile according to the size on page or the display of the metafile in its default size in C#.
type: docs
weight: 40
url: /net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

Gets or sets a value determining whether metafile rendering emulates the display of the metafile according to the size on page or the display of the metafile in its default size.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

## Remarks

When metafiles are displayed in MS Word, some graphics may be scaled according to the actual metafile size in pixels. I.e. even zooming may affect the metafile display.

When this value is set to `true`, Aspose.Words emulates rendering according to the metafile size on page. The size in pixels is calculated from the metafile size on the page and the specified [`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

When this value is set to `false`, Aspose.Words emulates metafile rendering to its default size in pixels.

This option is used only when metafile is rendered as vector graphics.

The default value is `true`.

### See Also

* class [MetafileRenderingOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
