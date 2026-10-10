---
title: "Aspose::Words::DocumentBuilder::InsertTableOfContents method"
linktitle: "InsertTableOfContents"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::InsertTableOfContents 方法。在 C++ 中向文档插入 TOC（目录）字段。"
type: docs
weight: 48000
url: /zh/cpp/aspose.words/documentbuilder/inserttableofcontents/
---
## DocumentBuilder::InsertTableOfContents method


在文档中插入 TOC（目录）字段。

```cpp
System::SharedPtr<Aspose::Words::Fields::Field> Aspose::Words::DocumentBuilder::InsertTableOfContents(const System::String &switches)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 开关 | const System::String\& | TOC 字段的开关。 |
## 备注


此方法将在文档的当前位置插入一个 TOC（目录）字段。

Word 文档中的目录可以通过多种方式构建，并使用各种选项进行格式化。目录的构建和显示方式由 Microsoft Word 的字段开关控制。

指定这些开关的最简方法是使用 Insert->Reference->Index 和 [Tables](../../../aspose.words.tables/) 菜单在 Word 文档中插入并配置目录，然后打开字段代码显示以查看开关。您可以在 Microsoft Word 中按 Alt+F9 切换字段代码的显示状态。

例如，在创建目录后，文档中会插入以下字段：**%{ TOC \\o \"1-3\" \\h \\z }**。您可以复制 **%\\o \"1-3\" \\h \\z** 并将其用作开关参数。

请注意，[InsertTableOfContents()](../) 只会插入 TOC 字段，但不会实际生成目录。目录会在字段更新时由 Microsoft Word 构建。

如果使用此方法插入目录后在 Microsoft Word 中打开文件，您将看不到目录，因为 TOC 字段尚未更新。

在 Microsoft Word 中，打开文档时字段不会自动更新，但您可以随时按 F9 来更新文档中的字段。

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

* Class [Field](../../../aspose.words.fields/field/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
