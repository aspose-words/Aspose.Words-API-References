---
title: Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 method
linktitle: get_ExportFontsAsBase64
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 method. Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is false in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_exportfontsasbase64/
---
## HtmlSaveOptions::get_ExportFontsAsBase64 method


Specifies whether fonts resources should be embedded to HTML in Base64 encoding. Default is **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64() const
```

## Remarks


By default, fonts are written to separate files. If this option is set to **true**, fonts will be embedded into the document's CSS in Base64 encoding.

## Examples



Shows how to save a .html document with images embedded inside it. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportImagesAsBase64(exportImagesAsBase64);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"<img src=\"data:image/png;base64") : outDocContents.Contains(u"<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```


Shows how to embed fonts inside a saved HTML document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontsAsBase64(true);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::Embedded);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
