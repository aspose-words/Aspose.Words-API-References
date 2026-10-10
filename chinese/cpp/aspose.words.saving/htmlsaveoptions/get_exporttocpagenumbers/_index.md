---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers 方法"
linktitle: "get_ExportTocPageNumbers"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers 方法。指定在保存为 HTML、MHTML 和 EPUB 时是否在目录中写入页码。默认在 C++ 中为 false。"
type: docs
weight: 29000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exporttocpagenumbers/
---
## HtmlSaveOptions::get_ExportTocPageNumbers method


指定在保存 HTML、MHTML 和 EPUB 时是否在目录中写入页码。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers() const
```


## 示例



展示在将包含目录的文档保存为 .html 时如何显示页码。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 插入目录，然后使用 "Heading" 格式的段落填充文档
// 样式，目录将其作为条目捕获。每个条目将在左侧显示标题段落，
// 以及右侧包含标题的页码。
auto fieldToc = System::ExplicitCast<Aspose::Words::Fields::FieldToc>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldTOC, true));

builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 1");
builder->Writeln(u"Entry 2");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 3");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Entry 4");
fieldToc->UpdatePageNumbers();
doc->UpdateFields();

// HTML 文档没有页面。如果我们将此文档保存为 HTML，
// 我们的目录显示的页码将没有意义。
// 当我们将文档保存为 HTML 时，可以传递一个 SaveOptions 对象以从目录中省略这些页码。
// 如果我们将 "ExportTocPageNumbers" 标志设置为 "true",
// 每个目录条目将显示标题、分隔符和页码，保持其在 Microsoft Word 中的外观。
// 如果我们将 "ExportTocPageNumbers" 标志设置为 "false",
// 保存操作将省略分隔符和页码，并保留每个条目的标题完整。
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportTocPageNumbers(exportTocPageNumbers);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span>Entry 1</span>") + u"<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " + u"-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" + u"<span>2</span>" + u"</p>"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<span>Entry 2</span>" + u"</p>"));
}
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
