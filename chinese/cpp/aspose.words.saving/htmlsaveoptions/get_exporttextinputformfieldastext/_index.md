---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText method"
linktitle: "get_ExportTextInputFormFieldAsText"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText method. 控制文本输入表单字段如何保存为 HTML 或 MHTML。默认值在 C++ 中为 false。"
type: docs
weight: 28000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exporttextinputformfieldastext/
---
## HtmlSaveOptions::get_ExportTextInputFormFieldAsText method


控制文本输入表单字段保存到 HTML 或 MHTML 的方式。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText() const
```

## 备注


当设置为 **true** 时，导出文本输入表单字段为普通文本。当设置为 **false** 时，导出 Word 文本输入表单字段为 HTML 中的 INPUT 元素。

导出为 EPUB 时，文本输入表单字段始终以文本形式保存，因为该格式的要求。

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
