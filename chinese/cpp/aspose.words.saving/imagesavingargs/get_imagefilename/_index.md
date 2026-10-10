---
title: "Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName 方法"
linktitle: "get_ImageFileName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName 方法。获取或设置在 C++ 中图像将保存到的文件名（不含路径）。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/imagesavingargs/get_imagefilename/
---
## ImageSavingArgs::get_ImageFileName method


获取或设置图像将要保存的文件名（不含路径）。

```cpp
System::String Aspose::Words::Saving::ImageSavingArgs::get_ImageFileName() const
```

## 备注


此属性允许您重新定义在导出为 HTML 时图像文件名的生成方式。

当事件触发时，此属性包含由 Aspose.Words 生成的文件名。您可以更改此属性的值，以将图像保存到其他文件。请注意，文件名必须唯一。

Aspose.Words 在导出为 HTML 格式时会自动为每个嵌入的图像生成唯一的文件名。文件名的生成方式取决于您是将文档保存为文件还是保存为流。

当将文档保存为文件时，生成的图像文件名类似于 *%<document base file name>.<image number>.<extension>*。

当将文档保存为流时，生成的图像文件名类似于 *Aspose.Words.<document guid>.<image number>.<extension>*。

[ImageFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to HTML using the document file name, the [ImagesFolder](../../htmlsaveoptions/get_imagesfolder/) and [ImagesFolderAlias](../../htmlsaveoptions/get_imagesfolderalias/) properties.

## 另见

* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
