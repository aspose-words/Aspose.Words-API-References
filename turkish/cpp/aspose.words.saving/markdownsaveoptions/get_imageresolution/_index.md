---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution yöntemi"
linktitle: "get_ImageResolution"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution yöntemi. Markdown formatına dışa aktarırken görüntüler için çıkış çözünürlüğünü belirtir. Varsayılan değer C++'da %96 dpi'dir."
type: docs
weight: 3750
url: /tr/cpp/aspose.words.saving/markdownsaveoptions/get_imageresolution/
---
## MarkdownSaveOptions::get_ImageResolution method


Markdown'a dışa aktarırken görüntüler için çıktı çözünürlüğünü belirtir. Varsayılan **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution() const
```


## Örnekler



Görüntüler için çıkış çözünürlüğünün nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ImageResolution(300);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

## Ayrıca Bakınız

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
