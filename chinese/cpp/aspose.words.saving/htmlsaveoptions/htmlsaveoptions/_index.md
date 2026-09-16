---
title: "Aspose::Words::Saving::HtmlSaveOptions::HtmlSaveOptions 构造函数"
linktitle: "HtmlSaveOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::HtmlSaveOptions 构造函数。初始化此类的新实例，可用于在 C++ 中将文档保存为 Html 格式。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/htmlsaveoptions/
---
## HtmlSaveOptions::HtmlSaveOptions() constructor


初始化此类的新实例，可用于将文档保存为 [Html](../../../aspose.words/saveformat/) 格式。

```cpp
Aspose::Words::Saving::HtmlSaveOptions::HtmlSaveOptions()
```


## 示例



展示如何在将文档保存为 .epub 时使用特定的编码。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// 使用 SaveOptions 对象来指定我们将要保存的文档的编码。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// 默认情况下，输出的 .epub 文档的所有内容都位于一个 HTML 部分中。
// 拆分条件允许我们将文档划分为多个 HTML 部分。
// 我们将设置条件，以将文档拆分为标题段落。
// 这对于无法读取大于特定大小的 HTML 文件的阅读器很有用。
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// 指定我们要导出文档属性。
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## HtmlSaveOptions::HtmlSaveOptions(Aspose::Words::SaveFormat) constructor


初始化此类的新实例，可用于将文档保存为 [Html](../../../aspose.words/saveformat/)、[Mhtml](../../../aspose.words/saveformat/)、[Epub](../../../aspose.words/saveformat/)、[Azw3](../../../aspose.words/saveformat/) 或 [Mobi](../../../aspose.words/saveformat/) 格式。

```cpp
Aspose::Words::Saving::HtmlSaveOptions::HtmlSaveOptions(Aspose::Words::SaveFormat saveFormat)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| saveFormat | Aspose::Words::SaveFormat | 可以是 [Html](../../../aspose.words/saveformat/)、[Mhtml](../../../aspose.words/saveformat/)、[Epub](../../../aspose.words/saveformat/)、[Azw3](../../../aspose.words/saveformat/) 或 [Mobi](../../../aspose.words/saveformat/)。 |

## 示例



展示如何将文档保存为特定版本的 HTML。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_HtmlVersion(htmlVersion);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HtmlVersions.html", options);

// 我们的 HTML 文档将有细微差异，以兼容不同的 HTML 版本。
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.HtmlVersions.html");

switch (htmlVersion)
{
    case Aspose::Words::Saving::HtmlVersion::Html5:
        ASSERT_TRUE(outDocContents.Contains(u"<a id=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<a id=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<table style=\"padding:0pt; -aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\">"));
        break;

    case Aspose::Words::Saving::HtmlVersion::Xhtml:
        ASSERT_TRUE(outDocContents.Contains(u"<a name=\"_Toc76372689\"></a>"));
        ASSERT_TRUE(outDocContents.Contains(u"<ul type=\"disc\" style=\"margin:0pt; padding-left:0pt\">"));
        ASSERT_TRUE(outDocContents.Contains(u"<table cellspacing=\"0\" cellpadding=\"0\" style=\"-aw-border:0.5pt single #000000; -aw-border-insideh:0.5pt single #000000; -aw-border-insidev:0.5pt single #000000; border-collapse:collapse\""));
        break;

}
```

## 另见

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
