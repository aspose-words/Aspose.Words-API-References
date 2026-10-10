---
title: "Aspose::Words::Saving::ExportListLabels 枚举"
linktitle: "ExportListLabels"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ExportListLabels 枚举。指定列表标签在 C++ 中如何导出到 HTML、MHTML 和 EPUB。"
type: docs
weight: 56000
url: /zh/cpp/aspose.words.saving/exportlistlabels/
---
## ExportListLabels enum


指定列表标签如何导出为 HTML、MHTML 和 EPUB。

```cpp
enum class ExportListLabels
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 自动 | 0 | 以自动模式输出列表标签。尽可能使用 HTML 原生元素。 |
| AsInlineText | 1 | 将所有列表标签输出为内联文本。 |
| ByHtmlTags | 2 | 将所有列表标签输出为 HTML 原生元素。 |


## 示例



展示如何将列表导出配置为 HTML。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Lists::List> list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::NumberDefault);
builder->get_ListFormat()->set_List(list);

builder->Writeln(u"Default numbered list item 1.");
builder->Writeln(u"Default numbered list item 2.");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Default numbered list item 3.");
builder->get_ListFormat()->RemoveNumbers();

list = doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::OutlineHeadingsLegal);
builder->get_ListFormat()->set_List(list);

builder->Writeln(u"Outline legal heading list item 1.");
builder->Writeln(u"Outline legal heading list item 2.");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Outline legal heading list item 3.");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Outline legal heading list item 4.");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Outline legal heading list item 5.");
builder->get_ListFormat()->RemoveNumbers();

// 在将文档保存为 HTML 时，我们可以传入一个 SaveOptions 对象
// 以决定文档将使用哪些 HTML 元素来表示列表。
// 将 "ExportListLabels" 属性设置为 "ExportListLabels.AsInlineText"
// 将通过格式化 span 来创建列表。
// 将 "ExportListLabels" 属性设置为 "ExportListLabels.Auto" 将使用 <p> 标签
// 在使用 <ol> 和 <li> 标签可能导致格式丢失的情况下构建列表。
// 将 "ExportListLabels" 属性设置为 "ExportListLabels.ByHtmlTags"
// 将使用 <ol> 和 <li> 标签来构建所有列表。
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportListLabels(exportListLabels);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.List.html", options);
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.List.html");

switch (exportListLabels)
{
    case Aspose::Words::Saving::ExportListLabels::AsInlineText:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-left:72pt; margin-bottom:0pt; text-indent:-18pt; -aw-import:list-item; -aw-list-level-number:1; -aw-list-number-format:'%1.'; -aw-list-number-styles:'lowerLetter'; -aw-list-number-values:'1'; -aw-list-padding-sml:9.67pt\">") + u"<span style=\"-aw-import:ignore\">" + u"<span>a.</span>" + u"<span style=\"width:9.67pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" + u"</span>" + u"<span>Default numbered list item 3.</span>" + u"</p>"));
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-left:43.2pt; margin-bottom:0pt; text-indent:-43.2pt; -aw-import:list-item; -aw-list-level-number:3; -aw-list-number-format:'%0.%1.%2.%3'; -aw-list-number-styles:'decimal decimal decimal decimal'; -aw-list-number-values:'2 1 1 1'; -aw-list-padding-sml:10.2pt\">") + u"<span style=\"-aw-import:ignore\">" + u"<span>2.1.1.1</span>" + u"<span style=\"width:10.2pt; font:7pt 'Times New Roman'; display:inline-block; -aw-import:spaces\">&#xa0;&#xa0;&#xa0;&#xa0;&#xa0;&#xa0; </span>" + u"</span>" + u"<span>Outline legal heading list item 5.</span>" + u"</p>"));
        break;

    case Aspose::Words::Saving::ExportListLabels::Auto:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<ol type=\"a\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">") + u"<li style=\"margin-left:31.33pt; padding-left:4.67pt\">" + u"<span>Default numbered list item 3.</span>" + u"</li>" + u"</ol>"));
        break;

    case Aspose::Words::Saving::ExportListLabels::ByHtmlTags:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<ol type=\"a\" style=\"margin-right:0pt; margin-left:0pt; padding-left:0pt\">") + u"<li style=\"margin-left:31.33pt; padding-left:4.67pt\">" + u"<span>Default numbered list item 3.</span>" + u"</li>" + u"</ol>"));
        break;

}
```

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
