---
title: Aspose::Words::Saving::MarkdownSaveOptions::set_ImageResolution method
linktitle: set_ImageResolution
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MarkdownSaveOptions::set_ImageResolution method. Specifies the output resolution for images when exporting to Markdown. Default is 96 dpi in C++.'
type: docs
weight: 11750
url: /cpp/aspose.words.saving/markdownsaveoptions/set_imageresolution/
---
## MarkdownSaveOptions::set_ImageResolution method


Specifies the output resolution for images when exporting to Markdown. Default is **96 dpi**.

```cpp
void Aspose::Words::Saving::MarkdownSaveOptions::set_ImageResolution(int32_t value)
```

## Examples


Shows how to set the output resolution for images.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rendering.docx"));

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ImageResolution(300);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImageResolution.md", saveOptions);
```
## See Also

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
