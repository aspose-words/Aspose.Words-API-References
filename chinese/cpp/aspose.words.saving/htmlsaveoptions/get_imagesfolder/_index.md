---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder 方法"
linktitle: "get_ImagesFolder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder 方法。指定在将文档导出为 HTML 格式时保存图像的物理文件夹。默认在 C++ 中为空字符串。"
type: docs
weight: 38000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolder/
---
## HtmlSaveOptions::get_ImagesFolder method


指定将文档导出为 HTML 格式时图像保存的物理文件夹。默认是空字符串。

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder() const
```

## 备注


当您以 HTML 格式保存 [Document](../../../aspose.words/document/) 时，Aspose.Words 需要将文档中嵌入的所有图像保存为独立文件。[ImagesFolder](./) 允许您指定图像保存的位置，而 [ImagesFolderAlias](../get_imagesfolderalias/) 则允许指定图像 URI 的构建方式。

如果您将文档保存为文件并提供文件名，Aspose.Words 默认会将图像保存在与文档文件相同的文件夹中。使用 [ImagesFolder](./) 可覆盖此行为。

如果您将文档保存到流中，Aspose.Words 没有用于保存图像的文件夹，但仍需将图像保存到某处。在这种情况下，您需要在 [ImagesFolder](./) 属性中指定一个可访问的文件夹，或通过 [ImageSavingCallback](../get_imagesavingcallback/) 事件处理程序提供自定义流。

如果 [ImagesFolder](./) 指定的文件夹不存在，它将自动创建。

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where images should be saved.

## 示例



展示如何在保存为 .html 后指定用于存储链接图像的文件夹。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// 设置一个选项，将表单字段导出为纯文本而不是 HTML 输入元素。
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
