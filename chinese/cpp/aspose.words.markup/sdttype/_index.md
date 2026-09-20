---
title: "Aspose::Words::Markup::SdtType 枚举"
linktitle: "SdtType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::SdtType 枚举。指定 C++ 中结构化文档标签 (SDT) 节点的类型。"
type: docs
weight: 21000
url: /zh/cpp/aspose.words.markup/sdttype/
---
## SdtType enum


指定结构化文档标签 (SDT) 节点的类型。

```cpp
enum class SdtType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 未为 SDT 分配类型。 |
| 参考文献 | 1 | SDT 表示一个参考文献条目。 |
| Citation | 2 | SDT 表示一个引用。 |
| Equation | 3 | SDT 表示一个公式。 |
| DropDownList | 4 | SDT 在文档中显示时表示一个下拉列表。 |
| ComboBox | 5 | SDT 在文档中显示时表示一个组合框。 |
| 日期 | 6 | SDT 在文档中显示时表示一个日期选择器。 |
| BuildingBlockGallery | 7 | SDT 表示一个构建块库类型。 |
| DocPartObj | 8 | SDT 表示一个文档部件类型。 |
| Group | 9 | SDT 在文档中显示时表示一个受限分组。 |
| Picture | 10 | SDT 在文档中显示时表示一幅图片。 |
| 富文本 | 11 | 当在文档中显示时，SDT 表示一个富文本框。 |
| 纯文本 | 12 | 当在文档中显示时，SDT 表示一个纯文本框。 |
| 复选框 | 13 | 当在文档中显示时，SDT 表示一个复选框。 |
| 重复节 | 14 | 当在文档中显示时，SDT 表示重复节类型。 |
| 重复节项 | 15 | SDT 表示重复节项。 |
| 实体选择器 | 16 | SDT 表示一个实体选择器，允许用户选择外部内容类型的实例。 |


## 示例



展示如何使用内容控件元素的样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 下面有两种方法将文档中的样式应用于结构化文档标签。
// 1 -  从文档的样式集合中应用样式对象：
System::SharedPtr<Aspose::Words::Style> quoteStyle = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Quote);
auto sdtPlainText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtPlainText->set_Style(quoteStyle);

// 2 -  按名称引用文档中的样式:
auto sdtRichText = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RichText, Aspose::Words::Markup::MarkupLevel::Inline);
sdtRichText->set_StyleName(u"Quote");

builder->InsertNode(sdtPlainText);
builder->InsertNode(sdtRichText);

ASSERT_EQ(Aspose::Words::NodeType::StructuredDocumentTag, sdtPlainText->get_NodeType());

System::SharedPtr<Aspose::Words::NodeCollection> tags = doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTag, true);

for (auto&& node : System::IterateOver(tags))
{
    auto sdt = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(node);

    std::cout << sdt->get_WordOpenXMLMinimal() << std::endl;

    ASSERT_EQ(Aspose::Words::StyleIdentifier::Quote, sdt->get_Style()->get_StyleIdentifier());
    ASSERT_EQ(u"Quote", sdt->get_StyleName());
}
```


展示如何使用 XML 部分中的数据填充表格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Markup::CustomXmlPart> xmlPart = doc->get_CustomXmlParts()->Add(u"Books", System::String(u"<books>") + u"<book>" + u"<title>Everyday Italian</title>" + u"<author>Giada De Laurentiis</author>" + u"</book>" + u"<book>" + u"<title>The C Programming Language</title>" + u"<author>Brian W. Kernighan, Dennis M. Ritchie</author>" + u"</book>" + u"<book>" + u"<title>Learning XML</title>" + u"<author>Erik T. Ray</author>" + u"</book>" + u"</books>");

// 为来自 XML 内容的数据创建标题。
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Title");
builder->InsertCell();
builder->Write(u"Author");
builder->EndRow();
builder->EndTable();

// 创建一个内部包含重复节的表格。
auto repeatingSectionSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSection, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book", System::String::Empty);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionSdt);

// 在重复节内部添加重复节项并将其标记为行。
// 此表格将为我们在 XML 文档中找到的每个元素创建一行
// 使用 "/books[1]/book" XPath，共有三个。
auto repeatingSectionItemSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::RepeatingSectionItem, Aspose::Words::Markup::MarkupLevel::Row);
repeatingSectionSdt->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(repeatingSectionItemSdt);

auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
repeatingSectionItemSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// 将 XML 数据映射到已创建的表格单元格，以显示每本书的标题和作者。
auto titleSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
titleSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/title[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(titleSdt);

auto authorSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Cell);
authorSdt->get_XmlMapping()->SetMapping(xmlPart, u"/books[1]/book[1]/author[1]", System::String::Empty);
row->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(authorSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.RepeatingSectionItem.docx");
```


展示如何在行级别创建组结构化文档标签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// 在行级别创建组结构化文档标签。
auto groupSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Group, Aspose::Words::Markup::MarkupLevel::Row);
table->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(groupSdt);
groupSdt->set_IsShowingPlaceholderText(false);
groupSdt->RemoveAllChildren();

// 创建结构化文档标签的子行。
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
groupSdt->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

builder->EndTable();

// 插入单元格内容。
cell->EnsureMinimum();
builder->MoveTo(cell->get_LastParagraph());
builder->Write(u"Lorem ipsum dolor.");

// 在表格后插入文本。
builder->MoveTo(table->get_NextSibling());
builder->Write(u"Nulla blandit nisi.");

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.SdtAtRowLevel.docx");
```


展示如何创建引用类型的结构化文档标签。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto sdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Citation, Aspose::Words::Markup::MarkupLevel::Inline);
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(sdt);

// 创建引用字段。
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToParagraph(0, -1);
builder->InsertField(u"CITATION Ath22 \\l 1033 ", u"(John Lennon, 2022)");

// 将字段移动到结构化文档标签。
while (sdt->get_NextSibling() != nullptr)
{
    sdt->AppendChild<System::SharedPtr<Aspose::Words::Node>>(sdt->get_NextSibling());
}

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Citation.docx");
```

## 另见

* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
