---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional 方法"
linktitle: "get_ExportXhtmlTransitional"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional 方法。指定在保存为 HTML 或 MHTML 时是否写入 DOCTYPE 声明。为 true 时，在根元素之前在文档中写入 DOCTYPE 声明。默认值为 false。保存为 EPUB 或 HTML5（Html5）时，始终在 C++ 中写入 DOCTYPE 声明。"
type: docs
weight: 30000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exportxhtmltransitional/
---
## HtmlSaveOptions::get_ExportXhtmlTransitional method


指定在保存为 HTML 或 MHTML 时是否写入 DOCTYPE 声明。为 **true** 时，在根元素之前在文档中写入 DOCTYPE 声明。默认值为 **false**。保存为 EPUB 或 HTML5（[Html5](../../htmlversion/)）时，始终写入 DOCTYPE 声明。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional() const
```

## 备注


无论此设置如何，Aspose.Words 始终生成符合规范的 HTML。

当 **true** 时，HTML 输出文档的开头将如下所示：


```cpp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
             <!DOCTYPE html
                   PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
             "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
             <html xmlns="http://www.w3.org/1999/xhtml" xml:lang="en" lang="en">
```


Aspose.Words 旨在根据 XHTML 1.0 Transitional 规范输出 XHTML，但输出并不总是能够通过 DTD 验证。Microsoft Word 文档中的某些结构很难或根本无法映射到能够通过 XHTML 架构验证的文档。例如，XHTML 不允许嵌套列表（UL 不能嵌套在另一个 UL 元素中），但在 Microsoft Word 文档中多级列表却经常出现。

## 示例



展示在将文档转换为 Xhtml 1.0 过渡标准时如何显示 DOCTYPE 标头。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(Aspose::Words::Saving::HtmlVersion::Xhtml);
options->set_ExportXhtmlTransitional(showDoctypeDeclaration);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// 只有在将 "ExportXhtmlTransitional" 标志设置为 "true" 时，我们的文档才会包含 DOCTYPE 声明标头。
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportXhtmlTransitional.html");
System::String newLine = System::Environment::get_NewLine();

if (showDoctypeDeclaration)
{
    ASSERT_TRUE(outDocContents.Contains(System::String::Format(u"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{0}", newLine) + System::String::Format(u"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">{0}", newLine) + u"<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<html>"));
}
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
