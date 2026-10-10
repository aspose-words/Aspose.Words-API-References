---
title: "Aspose::Words::DocumentBuilder::DocumentBuilder 构造函数"
linktitle: "DocumentBuilder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::DocumentBuilder 构造函数。在 C++ 中初始化此类的新实例。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder::DocumentBuilder() constructor


初始化此类的新实例。

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder()
```


## 示例



展示如何使用 [DocumentBuilder](../) 插入格式化文本。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 指定字体格式，然后添加文本。
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```

## 另见

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::Document\>\&) constructor


初始化此类的新实例。

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::Document> &doc)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | 要附加的 [Document](../../document/) 对象。 |

## 示例



展示如何使用标题样式作为条目，将目录（TOC）插入文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 在文档的首页插入目录。
// 配置目录以捕获标题级别 1 到 3 的段落。
// 此外，将其条目设置为超链接，以便我们
// 在 Microsoft Word 中左击时跳转到标题所在位置。
builder->InsertTableOfContents(u"\\o \"1-3\" \\h \\z \\u");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// 通过添加带有标题样式的段落来填充目录。
// 每个级别在 1 到 3 之间的标题都会在目录中创建一个条目。
builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 1.1");
builder->Writeln(u"Heading 1.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading1);
builder->Writeln(u"Heading 2");
builder->Writeln(u"Heading 3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.1");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading3);
builder->Writeln(u"Heading 3.1.1");
builder->Writeln(u"Heading 3.1.2");
builder->Writeln(u"Heading 3.1.3");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading4);
builder->Writeln(u"Heading 3.1.3.1");
builder->Writeln(u"Heading 3.1.3.2");

builder->get_ParagraphFormat()->set_StyleIdentifier(Aspose::Words::StyleIdentifier::Heading2);
builder->Writeln(u"Heading 3.2");
builder->Writeln(u"Heading 3.3");

// 目录是需要更新以显示最新结果的字段类型。
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertToc.docx");
```

## 另见

* Class [Document](../../document/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) constructor


初始化此类的新实例。

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::Document> &doc, const System::SharedPtr<Aspose::Words::DocumentBuilderOptions> &options)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | 要附加的 [Document](../../document/) 对象。 |
| options | const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\& | 文档构建过程的附加选项。 |

## 示例



展示如何忽略后续内容的表格格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// 在表格之前添加内容。
// 默认字体大小为 12。
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// 更改表格内部的字体大小。
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// 如果 ContextTableFormatting 为 true，则表格格式不会应用于后续内容。
// 如果 ContextTableFormatting 为 false，则表格格式将在之后的内容上应用。
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## 另见

* Class [Document](../../document/)
* Class [DocumentBuilderOptions](../../documentbuilderoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::DocumentBuilder(const System::SharedPtr\<Aspose::Words::DocumentBuilderOptions\>\&) constructor


初始化此类的新实例。

```cpp
Aspose::Words::DocumentBuilder::DocumentBuilder(const System::SharedPtr<Aspose::Words::DocumentBuilderOptions> &options)
```


## 示例



展示如何忽略后续内容的表格格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// 在表格之前添加内容。
// 默认字体大小为 12。
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// 更改表格内部的字体大小。
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// 如果 ContextTableFormatting 为 true，则表格格式不会应用于后续内容。
// 如果 ContextTableFormatting 为 false，则表格格式将在之后的内容上应用。
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## 另见

* Class [DocumentBuilderOptions](../../documentbuilderoptions/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
