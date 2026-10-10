---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias 方法"
linktitle: "get_ImagesFolderAlias"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias 方法。指定用于构建写入文档的图像 URI 的文件夹名称。默认值在 C++ 中为空字符串。"
type: docs
weight: 5500
url: /zh/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolderalias/
---
## MarkdownSaveOptions::get_ImagesFolderAlias method


指定用于构建写入文档中的图像 URI 的文件夹名称。默认是空字符串。

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias() const
```

## 备注


当您以 [Markdown](../../../aspose.words/saveformat/) 格式保存 [Document](../../../aspose.words/document/) 时，Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。[ImagesFolder](../get_imagesfolder/) 允许您指定图像的保存位置，而 [ImagesFolderAlias](./) 则允许指定图像 URI 的构建方式。

如果 [ImagesFolderAlias](./) 不是空字符串，则写入 Markdown 的图像 URI 将是 *ImagesFolderAlias + <image file name>*。

如果 [ImagesFolderAlias](./) 是空字符串，则写入 Markdown 的图像 URI 将是 *ImagesFolder + <image file name>*。

如果 [ImagesFolderAlias](./) 设置为 '.'（点），则无论其他选项如何，图像文件名都会以不带路径的形式写入 Markdown。

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
