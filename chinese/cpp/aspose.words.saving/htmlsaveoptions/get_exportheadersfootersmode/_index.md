---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode 方法"
linktitle: "get_ExportHeadersFootersMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode 方法。指定标题和页脚如何输出到 HTML、MHTML 或 EPUB。在 C++ 中，默认值为 HTML/MHTML 的 PerSection 和 EPUB 的 None。"
type: docs
weight: 18000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exportheadersfootersmode/
---
## HtmlSaveOptions::get_ExportHeadersFootersMode method


指定标题和页脚如何输出到 HTML、MHTML 或 EPUB。默认值为 HTML/MHTML 的 [PerSection](../../exportheadersfootersmode/) 和 EPUB 的 [None](../../exportheadersfootersmode/)。

```cpp
Aspose::Words::Saving::ExportHeadersFootersMode Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode() const
```

## 备注


由于 HTML 没有分页，难以有意义地将标题和页脚输出为 HTML。

当此属性为 [PerSection](../../exportheadersfootersmode/) 时，Aspose.Words 仅在每个节的开头和结尾导出主页眉和页脚。

当其为 [FirstSectionHeaderLastSectionFooter](../../exportheadersfootersmode/) 时，仅导出第一个主页眉和最后一个主页脚（包括链接到前一个的页脚）。

您可以通过将此属性设置为 [None](../../exportheadersfootersmode/) 来完全禁用页眉和页脚的导出。

## 示例



展示在将文档保存为 HTML 时如何省略标题/页脚。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// 此文档包含标题和页脚。我们可以通过 "HeadersFooters" 集合访问它们。
ASSERT_EQ(u"First header", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());

// 像 .html 这样的格式不会将文档拆分为页面，因此标题/页脚的功能将不同。
// 它们在我们使用 Microsoft Word 将文档打开为 .docx 时的表现。
// 如果我们将包含标题/页脚的文档转换为 html，转换过程会将标题/页脚合并到正文中。
// 我们可以使用 SaveOptions 对象在转换为 html 时省略标题/页脚。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
saveOptions->set_ExportHeadersFootersMode(Aspose::Words::Saving::ExportHeadersFootersMode::None);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html", saveOptions);

// 打开我们保存的文档，并验证其中不包含标题文本
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html");

ASSERT_FALSE(doc->get_Range()->get_Text().Contains(u"First header"));
```

## 另见

* Enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
