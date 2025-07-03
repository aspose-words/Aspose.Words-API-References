---
title: Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64 method
linktitle: get_ExportImagesAsBase64
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64 method. Specifies whether images are saved in Base64 format to the output HTML, MHTML or EPUB. Default is false in C++.'
type: docs
weight: 19000
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
