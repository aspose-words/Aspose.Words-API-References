---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder 方法"
linktitle: "get_ImagesFolder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder 方法。指定将文档导出为 Markdown 格式时保存图像的物理文件夹。默认在 C++ 中为空字符串。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolder/
---
## MarkdownSaveOptions::get_ImagesFolder method


指定将文档导出为 [Markdown](../../../aspose.words/saveformat/) 格式时保存图像的物理文件夹。默认为空字符串。

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder() const
```

## 备注


当您以 [Markdown](../../../aspose.words/saveformat/) 格式保存 [Document](../../../aspose.words/document/) 时，Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。[ImagesFolder](./) 允许您指定图像的保存位置。

如果您将文档保存为文件并提供文件名，Aspose.Words 默认会将图像保存在与文档文件相同的文件夹中。使用 [ImagesFolder](./) 可覆盖此行为。

如果您将文档保存到流中，Aspose.Words 没有用于保存图像的文件夹，但仍需要在某处保存图像。在这种情况下，您需要在 [ImagesFolder](./) 属性中指定一个可访问的文件夹。

如果 [ImagesFolder](./) 指定的文件夹不存在，它将自动创建。

## 示例



展示如何指定用于构建图像 URI 的文件夹名称。
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

builder->Writeln(u"Some image below:");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

System::String imagesFolder = System::IO::Path::Combine(get_ArtifactsDir(), u"ImagesDir");
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
// 使用 "ImagesFolder" 属性将本地文件系统中的文件夹指定为
// Aspose.Words 将保存文档中所有链接的图像。
saveOptions->set_ImagesFolder(imagesFolder);
// Use the "ImagesFolderAlias" property to use this folder
// 在构建图像 URI 时，而不是使用图像文件夹的名称。
saveOptions->set_ImagesFolderAlias(u"http://example.com/images");

builder->get_Document()->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

## 另见

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
