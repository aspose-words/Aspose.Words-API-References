---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel 方法"
linktitle: "get_DocumentSplitHeadingLevel"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel 方法。指定在文档中拆分的标题的最大级别。默认值在 C++ 中为 %2。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_documentsplitheadinglevel/
---
## HtmlSaveOptions::get_DocumentSplitHeadingLevel method


指定拆分文档时的最大标题级别。默认值为 **%2**。

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel() const
```

## 备注


当 [DocumentSplitCriteria](../get_documentsplitcriteria/) 包含 [HeadingParagraph](../../documentsplitcriteria/) 且此属性设置为 1 到 9 的值时，文档将在使用 **Heading 1**、**Heading 2**、**Heading 3** 等样式的段落处进行拆分，直至指定的标题级别。

默认情况下，只有 **Heading 1** 和 **Heading 2** 段落会导致文档被拆分。将此属性设置为零将导致文档根本不会在标题段落处拆分。

## 示例



展示如何按标题将输出的 HTML 文档拆分为多个部分。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 我们使用 "Heading" 样式格式化的每个段落都可以充当标题。
// 每个标题还可能具有标题级别，由其标题样式的编号决定。
// 以下标题的级别为 1-3。
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #1");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #2");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #3");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Heading #4");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 2"));
builder->Writeln(u"Heading #5");
builder->get_ParagraphFormat()->set_Style(builder->get_Document()->get_Styles()->idx_get(u"Heading 3"));
builder->Writeln(u"Heading #6");

// 创建一个 HtmlSaveOptions 对象并将拆分标准设置为 "HeadingParagraph"。
// 这些标准将把文档在具有 "Heading" 样式的段落处拆分为多个较小的文档，
// 并将每个文档保存为本地文件系统中的单独 HTML 文件。
// 我们还将设置最大标题级别，将文档拆分为 2 级。
// 保存文档时会在 1 级和 2 级标题处进行拆分，但不会在 3 到 9 级标题处拆分。
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);
options->set_DocumentSplitHeadingLevel(2);

// 我们的文档有四个 1 - 2 级的标题。其中一个标题将不会是
// 拆分点，因为它位于文档的开头。
// 保存操作将在三个位置拆分我们的文档，生成四个较小的文档。
doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html", options);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels.html");

ASSERT_EQ(u"Heading #1", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-01.html");

ASSERT_EQ(System::String(u"Heading #2\r") + u"Heading #3", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-02.html");

ASSERT_EQ(u"Heading #4", doc->GetText().Trim());

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HtmlSaveOptions.HeadingLevels-03.html");

ASSERT_EQ(System::String(u"Heading #5\r") + u"Heading #6", doc->GetText().Trim());
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
