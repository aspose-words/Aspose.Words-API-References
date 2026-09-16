---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution 方法"
linktitle: "get_ImageResolution"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution 方法。指定导出为 Markdown 时图像的输出分辨率。默认值在 C++ 中为 %96 dpi。"
type: docs
weight: 3750
url: /zh/cpp/aspose.words.saving/markdownsaveoptions/get_imageresolution/
---
## MarkdownSaveOptions::get_ImageResolution method


指定导出为 Markdown 时图像的输出分辨率。默认值为 **%96 dpi**。

```cpp
int32_t Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution() const
```


## 示例



展示如何设置图像的输出分辨率。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ImageResolution(300);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

## 另见

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
