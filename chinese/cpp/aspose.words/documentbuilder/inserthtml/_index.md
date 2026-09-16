---
title: "Aspose::Words::DocumentBuilder::InsertHtml 方法"
linktitle: "InsertHtml"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertHtml 方法。在 C++ 中将 HTML 字符串插入文档。"
type: docs
weight: 37000
url: /zh/cpp/aspose.words/documentbuilder/inserthtml/
---
## DocumentBuilder::InsertHtml(const System::String\&) method


将 HTML 字符串插入文档。

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| html | const System::String\& | 要插入文档的 HTML 字符串。 |

## 示例



展示如何使用文档生成器将 HTML 内容插入文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

const System::String html = System::String(u"<p align='right'>Paragraph right</p>") + u"<b>Implicit paragraph left</b>" + u"<div align='center'>Div center</div>" + u"<h1 align='left'>Heading 1 left.</h1>";

builder->InsertHtml(html);

// 插入 HTML 代码会将每个元素的格式解析为等效的文档文本格式。
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

ASSERT_EQ(u"Paragraph right", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Implicit paragraph left", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());
ASSERT_TRUE(paragraphs->idx_get(1)->get_Runs()->idx_get(0)->get_Font()->get_Bold());

ASSERT_EQ(u"Div center", paragraphs->idx_get(2)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Center, paragraphs->idx_get(2)->get_ParagraphFormat()->get_Alignment());

ASSERT_EQ(u"Heading 1 left.", paragraphs->idx_get(3)->GetText().Trim());
ASSERT_EQ(u"Heading 1", paragraphs->idx_get(3)->get_ParagraphFormat()->get_Style()->get_Name());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtml.docx");
```

## 另见

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, Aspose::Words::HtmlInsertOptions) method


将 HTML 字符串插入文档。允许指定其他选项。

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, Aspose::Words::HtmlInsertOptions options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| html | const System::String\& | 要插入文档的 HTML 字符串。 |
| options | Aspose::Words::HtmlInsertOptions | 在插入 HTML 字符串时使用的选项。 |

## 另见

* Enum [HtmlInsertOptions](../../htmlinsertoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertHtml(const System::String\&, bool) method


将 HTML 字符串插入文档。

```cpp
void Aspose::Words::DocumentBuilder::InsertHtml(const System::String &html, bool useBuilderFormatting)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| html | const System::String\& | 要插入文档的 HTML 字符串。 |
| useBuilderFormatting | bool | 一个值，指示是否使用在 [DocumentBuilder](../) 中指定的格式作为从 HTML 导入的文本的基础格式。 |
## 备注


您可以使用此方法插入 HTML 片段或完整的 HTML 文档。

当 *useBuilderFormatting* 为 **false** 时，[DocumentBuilder](../) 的格式被忽略，插入文本的格式基于默认的 HTML 格式。因此，文本看起来就像在浏览器中渲染的那样。

当 *useBuilderFormatting* 为 **true** 时，插入文本的格式基于 [DocumentBuilder](../) 的格式，文本看起来好像是使用 [Write()](../) 插入的。

## 示例



展示如何在插入 HTML 内容时应用文档构建器的格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 为构建器设置文本对齐方式，插入一个具有指定对齐方式的 HTML 段落，以及一个未指定对齐方式的段落。
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Distributed);
builder->InsertHtml(System::String(u"<p align='right'>Paragraph 1.</p>") + u"<p>Paragraph 2.</p>", useBuilderFormatting);

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// 第一段指定了对齐方式。当 InsertHtml 解析 HTML 代码时，
// HTML 代码中找到的段落对齐值始终会覆盖文档构建器的值。
ASSERT_EQ(u"Paragraph 1.", paragraphs->idx_get(0)->GetText().Trim());
ASSERT_EQ(Aspose::Words::ParagraphAlignment::Right, paragraphs->idx_get(0)->get_ParagraphFormat()->get_Alignment());

// 第二段未指定对齐方式。它可以使用
// 由构建器的值填充，这取决于我们传递给 InsertHtml 方法的标志。
ASSERT_EQ(u"Paragraph 2.", paragraphs->idx_get(1)->GetText().Trim());
ASSERT_EQ(useBuilderFormatting ? Aspose::Words::ParagraphAlignment::Distributed : Aspose::Words::ParagraphAlignment::Left, paragraphs->idx_get(1)->get_ParagraphFormat()->get_Alignment());

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHtmlWithFormatting.docx");
```

## 另见

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
