---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName 方法"
linktitle: "get_ResourceFileName"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName 方法。获取或设置资源将在 C++ 中保存的文件名（不含路径）。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/resourcesavingargs/get_resourcefilename/
---
## ResourceSavingArgs::get_ResourceFileName method


获取或设置资源将被保存到的文件名（不含路径）。

```cpp
System::String Aspose::Words::Saving::ResourceSavingArgs::get_ResourceFileName() const
```

## 备注


此属性允许您重新定义在导出为固定页面 HTML、SVG 或 Markdown 时资源文件名的生成方式。

当事件触发时，此属性包含 Aspose.Words 生成的文件名。您可以更改此属性的值，以将资源保存到其他文件。请注意，文件名必须唯一。

Aspose.Words 在导出为固定页面 HTML、SVG 或 Markdown 格式时，会自动为每个资源生成唯一的文件名。文件名的生成方式取决于您是将文档保存为文件还是保存为流。

当将文档保存为文件时，生成的资源文件名类似于 *%<document base file name>.<image number>.<extension>*。

当将文档保存为流时，生成的资源文件名类似于 *Aspose.Words.<document guid>.<image number>.<extension>*。

[ResourceFileName](./) must contain only the file name without the path. Aspose.Words determines the path for saving and the value of the **src** attribute for writing to fixed page HTML, SVG or Markdown using the document file name, the [ResourcesFolder](../../htmlfixedsaveoptions/get_resourcesfolder/) or [ResourcesFolder](../../svgsaveoptions/get_resourcesfolder/) and [ResourcesFolderAlias](../../htmlfixedsaveoptions/get_resourcesfolderalias/) or [ResourcesFolderAlias](../../svgsaveoptions/get_resourcesfolderalias/) or [ImagesFolder](../../markdownsaveoptions/get_imagesfolder/) or [ImagesFolderAlias](../../markdownsaveoptions/get_imagesfolderalias/) properties.

## 另见

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
