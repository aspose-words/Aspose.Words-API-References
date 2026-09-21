---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution‑metod"
linktitle: "get_ImageResolution"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution‑metod. Anger utdataupplösningen för bilder vid export till Markdown. Standard är %96 dpi i C++."
type: docs
weight: 3750
url: /sv/cpp/aspose.words.saving/markdownsaveoptions/get_imageresolution/
---
## MarkdownSaveOptions::get_ImageResolution method


Anger utskriftsupplösningen för bilder vid export till Markdown. Standard är **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution() const
```


## Exempel



Visar hur man ställer in utdataupplösningen för bilder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ImageResolution(300);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

## Se även

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
