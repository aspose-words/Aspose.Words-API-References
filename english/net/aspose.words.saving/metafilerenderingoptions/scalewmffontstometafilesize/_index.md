---
title: MetafileRenderingOptions.ScaleWmfFontsToMetafileSize
linktitle: ScaleWmfFontsToMetafileSize
second_title: Aspose.Words for .NET API Reference
description: MetafileRenderingOptions property. Gets or sets a value determining whether or not to scale fonts in WMF metafile according to metafile size on the page in C#.
type: docs
weight: 50
url: /net/aspose.words.saving/metafilerenderingoptions/scalewmffontstometafilesize/
---
## MetafileRenderingOptions.ScaleWmfFontsToMetafileSize property

Gets or sets a value determining whether or not to scale fonts in WMF metafile according to metafile size on the page.

```csharp
public bool ScaleWmfFontsToMetafileSize { get; set; }
```

## Remarks

When WMF metafiles are displayed in MS Word, fonts may be scaled according to actual metafile size on the page.

When this value is set to `true`, Aspose.Words emulates font scaling according to metafile size on the page.

When this value is set to `false`, Aspose.Words displays the fonts as metafile is rendered to its default size.

This option is used only when metafile is rendered as vector graphics.

The default value is `true`.

## Examples

Shows how to WMF fonts scaling according to metafile size on the page.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Set the "ScaleWmfFontsToMetafileSize" property to "true" to scale fonts
// that format text within WMF images according to the size of the metafile on the page.
// Set the "ScaleWmfFontsToMetafileSize" property to "false" to
// preserve the default scale of these fonts.
saveOptions.MetafileRenderingOptions.ScaleWmfFontsToMetafileSize = scaleWmfFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.FontsScaledToMetafileSize.pdf", saveOptions);
```

### See Also

* class [MetafileRenderingOptions](../)
* namespace [Aspose.Words.Saving](../../metafilerenderingoptions/)
* assembly [Aspose.Words](../../../)
