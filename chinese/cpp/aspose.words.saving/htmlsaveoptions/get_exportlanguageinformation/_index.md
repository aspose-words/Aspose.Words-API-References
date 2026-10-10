---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation 方法"
linktitle: "get_ExportLanguageInformation"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation 方法。指定是否将语言信息导出到 HTML、MHTML 或 EPUB。默认在 C++ 中为 false。"
type: docs
weight: 20000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exportlanguageinformation/
---
## HtmlSaveOptions::get_ExportLanguageInformation method


指定是否将语言信息导出到 HTML、MHTML 或 EPUB。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation() const
```

## 备注


当此属性设置为 **true** 时，Aspose.Words 会在指定语言的文档元素上输出 **lang** HTML 属性。这可能需要用于保留与语言相关的语义。

## 示例



展示如何在保存为 .html 时保留语言信息。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 使用构建器在不同地区设置下编写文本并进行格式化。
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US")->get_LCID());
builder->Writeln(u"Hello world!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-GB")->get_LCID());
builder->Writeln(u"Hello again!");

builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU")->get_LCID());
builder->Write(u"Привет, мир!");

// 在将文档保存为 HTML 时，我们可以传入一个 SaveOptions 对象
// 以保留或丢弃每个格式化文本的语言环境。
// 如果我们将 "ExportLanguageInformation" 标志设置为 "true",
// 输出的 HTML 文档将在 <span> 标签的 "lang" 属性中包含语言环境。
// 如果我们将 "ExportLanguageInformation" 标志设置为 "false',
// 输出的 HTML 文档中的文本将不包含任何语言环境信息。
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportLanguageInformation(exportLanguageInformation);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportLanguageInformation.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportLanguageInformation.html");

if (exportLanguageInformation)
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"en-GB\">Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span lang=\"ru-RU\">Привет, мир!</span>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello world!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Hello again!</span>"));
    ASSERT_TRUE(outDocContents.Contains(u"<span>Привет, мир!</span>"));
}
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
