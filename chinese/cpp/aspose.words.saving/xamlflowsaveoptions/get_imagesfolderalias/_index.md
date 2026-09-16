---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias 方法"
linktitle: "get_ImagesFolderAlias"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias 方法。指定用于构建写入 XAML 文档的图像 URI 的文件夹名称。默认在 C++ 中为空字符串。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolderalias/
---
## XamlFlowSaveOptions::get_ImagesFolderAlias method


指定用于构建写入 XAML 文档的图像 URI 的文件夹名称。默认是空字符串。

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias() const
```

## 备注


当您以 XAML 格式保存 [Document](../../../aspose.words/document/) 时，Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。[ImagesFolder](../get_imagesfolder/) 允许您指定图像的保存位置，而 [ImagesFolderAlias](./) 则允许指定图像 URI 的构建方式。

如果 [ImagesFolderAlias](./) 不是空字符串，则写入 XAML 的图像 URI 将是 *ImagesFolderAlias + <image file name>*。

如果 [ImagesFolderAlias](./) 是空字符串，则写入 XAML 的图像 URI 将是 *ImagesFolder + <image file name>*。

如果 [ImagesFolderAlias](./) 设置为 '.'（点），则无论其他选项如何，图像文件名都会以不带路径的形式写入 XAML。

## 另见

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
