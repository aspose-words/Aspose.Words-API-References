---
title: get_ExportFontsAsBase64
second_title: Aspose.Words for C++ API Reference
description: Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is false.
type: docs
weight: 196
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportfontsasbase64/
---
## HtmlSaveOptions.get_ExportFontsAsBase64 method


Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64() const
```


By default, fonts are written to separate files. If this option is set to **true**, fonts will be embedded into the document's CSS in Base64 encoding.

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

