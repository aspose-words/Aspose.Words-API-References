---
title: get_ScaleWmfFontsToMetafileSize
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value determining whether or not to scale fonts in WMF metafile according to metafile size on the page.
type: docs
weight: 66
url: /cpp/aspose.words.saving/metafilerenderingoptions/get_scalewmffontstometafilesize/
---
## MetafileRenderingOptions::get_ScaleWmfFontsToMetafileSize method


Gets or sets a value determining whether or not to scale fonts in WMF metafile according to metafile size on the page.

```cpp
bool Aspose::Words::Saving::MetafileRenderingOptions::get_ScaleWmfFontsToMetafileSize() const
```

## Remarks


When WMF metafiles are displayed in MS Word, fonts may be scaled according to actual metafile size on the page.

When this value is set to **true**, Aspose.Words emulates font scaling according to metafile size on the page.

When this value is set to **false**, Aspose.Words displays the fonts as metafile is rendered to its default size.

This option is used only when metafile is rendered as vector graphics.

The default value is **true**.

## Examples



Shows how to WMF fonts scaling according to metafile size on the page. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"WMF with text.docx");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto saveOptions = MakeObject<PdfSaveOptions>();

// Set the "ScaleWmfFontsToMetafileSize" property to "true" to scale fonts
// that format text within WMF images according to the size of the metafile on the page.
// Set the "ScaleWmfFontsToMetafileSize" property to "false" to
// preserve the default scale of these fonts.
saveOptions->get_MetafileRenderingOptions()->set_ScaleWmfFontsToMetafileSize(scaleWmfFonts);

doc->Save(ArtifactsDir + u"PdfSaveOptions.FontsScaledToMetafileSize.pdf", saveOptions);
```

## See Also

* Class [MetafileRenderingOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
