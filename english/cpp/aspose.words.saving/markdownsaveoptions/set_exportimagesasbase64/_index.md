---
title: Aspose::Words::Saving::MarkdownSaveOptions::set_ExportImagesAsBase64 method
linktitle: set_ExportImagesAsBase64
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownSaveOptions::set_ExportImagesAsBase64 method. Specifies whether images are saved in Base64 format to the output file. Default value is false in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.saving/markdownsaveoptions/set_exportimagesasbase64/
---
## MarkdownSaveOptions::set_ExportImagesAsBase64 method


Specifies whether images are saved in Base64 format to the output file. Default value is **false**.

```cpp
void Aspose::Words::Saving::MarkdownSaveOptions::set_ExportImagesAsBase64(bool value)
```

## Remarks


When this property is set to **true** images data are exported directly into the img elements and separate files are not created.
## Examples


Shows how to save a .md document with images embedded inside it.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Images.docx"));

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportImagesAsBase64(exportImagesAsBase64);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"data:image/jpeg;base64") : outDocContents.Contains(u"MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```
## See Also

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
