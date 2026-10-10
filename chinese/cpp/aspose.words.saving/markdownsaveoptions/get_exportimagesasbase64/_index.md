---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64 方法"
linktitle: "get_ExportImagesAsBase64"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64 方法。指定是否将图像以 Base64 格式保存到输出文件中。默认值在 C++ 中为 false。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.saving/markdownsaveoptions/get_exportimagesasbase64/
---
## MarkdownSaveOptions::get_ExportImagesAsBase64 method


指定图像是否以 Base64 格式保存到输出文件。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64() const
```

## 备注


当此属性设置为 **true** 时，图像数据会直接导出到 **img** 元素中，不会创建单独的文件。

## 示例



展示如何保存一个带有嵌入图像的 .md 文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportImagesAsBase64(exportImagesAsBase64);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"data:image/jpeg;base64") : outDocContents.Contains(u"MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

## 另见

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
