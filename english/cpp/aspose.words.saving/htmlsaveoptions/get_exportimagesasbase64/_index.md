---
title: get_ExportImagesAsBase64
second_title: Aspose.Words for C++ API Reference
description: Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is false.
type: docs
weight: 235
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportimagesasbase64/
---
## HtmlSaveOptions::get_ExportImagesAsBase64 method


Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64() const
```

## Remarks


When this property is set to **true** images data are exported directly into the **img** elements and separate files are not created.

## Examples



Shows how to save a .html document with images embedded inside it. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

auto options = MakeObject<HtmlSaveOptions>();
options->set_ExportImagesAsBase64(exportItemsAsBase64);
options->set_PrettyFormat(true);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.ExportImagesAsBase64.html", options);

String outDocContents = System::IO::File::ReadAllText(ArtifactsDir + u"HtmlSaveOptions.ExportImagesAsBase64.html");

ASSERT_TRUE(exportItemsAsBase64 ? outDocContents.Contains(u"<img src=\"data:image/png;base64")
                                : outDocContents.Contains(u"<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```


Shows how to embed fonts inside a saved HTML document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Rendering.docx");

auto options = MakeObject<HtmlSaveOptions>();
options->set_ExportFontsAsBase64(true);
options->set_CssStyleSheetType(CssStyleSheetType::Embedded);
options->set_PrettyFormat(true);

doc->Save(ArtifactsDir + u"HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
