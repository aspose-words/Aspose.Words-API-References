---
title: "Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder 方法"
linktitle: "get_ResourcesFolder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder 方法。指定在将文档导出为固定页面 Xaml 格式时，资源（图像和字体）保存的物理文件夹。在 C++ 中默认值为 null。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.saving/xamlfixedsaveoptions/get_resourcesfolder/
---
## XamlFixedSaveOptions::get_ResourcesFolder method


指定在将文档导出为固定页面 Xaml 格式时资源（图像和字体）保存的物理文件夹。默认值为 **null**。

```cpp
System::String Aspose::Words::Saving::XamlFixedSaveOptions::get_ResourcesFolder() const
```

## 备注


当您以固定页面 Xaml 格式保存 [Document](../../../aspose.words/document/) 时，Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。[ResourcesFolder](./) 允许您指定图像的保存位置，而 [ResourcesFolderAlias](../get_resourcesfolderalias/) 则允许指定图像 URI 的构建方式。

如果您将文档保存到文件并提供文件名，Aspose.Words 默认会将图像保存到文档文件所在的同一文件夹。使用 [ResourcesFolder](./) 可覆盖此行为。

如果您将文档保存到流中，Aspose.Words 没有用于保存图像的文件夹，但仍需将图像保存到某处。在这种情况下，您需要通过使用 [ResourcesFolder](./) 属性来指定一个可访问的文件夹。

## 另见

* Class [XamlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
