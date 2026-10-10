---
title: "Aspose::Words::BreakType enum"
linktitle: "BreakType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BreakType 枚举。指定文档中断点的类型（C++）。"
type: docs
weight: 82000
url: /zh/cpp/aspose.words/breaktype/
---
## BreakType enum


指定文档内部换行的类型。

```cpp
enum class BreakType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| ParagraphBreak | 0 | 段落之间的换行。 |
| PageBreak | 1 | 显式分页符。 |
| ColumnBreak | 2 | 显式列分隔符。 |
| SectionBreakContinuous | 3 | 指定在与前一节相同页面上开始新节。 |
| SectionBreakNewColumn | 4 | 指定在新列中开始新节。 |
| SectionBreakNewPage | 5 | 指定在新页面上开始新节。 |
| SectionBreakEvenPage | 6 | 指定在新的偶数页上开始新节。 |
| SectionBreakOddPage | 7 | 指定在奇数页上开始新节。 |
| LineBreak | 8 | 显式换行符。 |


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


展示如何对文档中的节应用和恢复页面设置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 修改构建器当前节的页面设置属性并添加文本。
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_VerticalAlignment(Aspose::Words::PageVerticalAlignment::Center);
builder->Writeln(u"This is the first section, which landscape oriented with vertically centered text.");

// 如果我们使用文档构建器开始新节，
// 它将继承构建器当前的页面设置属性。
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Orientation::Landscape, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Center, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

// 我们可以使用 "ClearFormatting" 方法将其页面设置属性恢复为默认值。
builder->get_PageSetup()->ClearFormatting();

ASSERT_EQ(Aspose::Words::Orientation::Portrait, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_Orientation());
ASSERT_EQ(Aspose::Words::PageVerticalAlignment::Top, doc->get_Sections()->idx_get(1)->get_PageSetup()->get_VerticalAlignment());

builder->Writeln(u"This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ClearFormatting.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
