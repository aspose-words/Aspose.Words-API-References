---
title: "Aspose::Words::Saving::ExportHeadersFootersMode 枚举"
linktitle: "ExportHeadersFootersMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ExportHeadersFootersMode 枚举。指定在 C++ 中标题和页脚如何导出到 HTML、MHTML 或 EPUB。"
type: docs
weight: 55000
url: /zh/cpp/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enum


指定页眉和页脚如何导出为 HTML、MHTML 或 EPUB。

```cpp
enum class ExportHeadersFootersMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 标题和页脚不被导出。 |
| PerSection | 1 | 主要标题和页脚在每个章节的开头和结尾处导出。 |
| FirstSectionHeaderLastSectionFooter | 2 | 第一节的主要标题在文档开头导出，主要页脚在文档末尾导出。 |
| FirstPageHeaderFooterPerSection | 3 | 每个章节的第一页标题和页脚在开头和结尾处导出。 |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
