---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder 方法"
linktitle: "get_ImagesFolder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder 方法。指定将文档导出为 XAML 格式时图像保存的物理文件夹。默认在 C++ 中为空字符串。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolder/
---
## XamlFlowSaveOptions::get_ImagesFolder method


指定在将文档导出为 XAML 格式时保存图像的物理文件夹。默认是空字符串。

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder() const
```

## 备注


当您以 XAML 格式保存 [Document](../../../aspose.words/document/) 时，Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。[ImagesFolder](./) 允许您指定图像的保存位置，而 [ImagesFolderAlias](../get_imagesfolderalias/) 则允许指定图像 URI 的构建方式。

如果您将文档保存为文件并提供文件名，Aspose.Words 默认会将图像保存在与文档文件相同的文件夹中。使用 [ImagesFolder](./) 可覆盖此行为。

如果您将文档保存到流中，Aspose.Words 没有用于保存图像的文件夹，但仍需将图像保存到某处。在这种情况下，您需要在 [ImagesFolder](./) 属性中指定一个可访问的文件夹，或通过 [ImageSavingCallback](../get_imagesavingcallback/) 事件处理程序提供自定义流。

## 另见

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
