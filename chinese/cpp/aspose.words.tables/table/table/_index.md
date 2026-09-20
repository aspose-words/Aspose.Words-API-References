---
title: "Aspose::Words::Tables::Table::Table constructor"
linktitle: "表格"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::Table 构造函数。用 C++ 初始化 Table 类的新实例。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.tables/table/table/
---
## Table::Table constructor


初始化 [Table](../) 类的新实例。

```cpp
Aspose::Words::Tables::Table::Table(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 文档 | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | 所属文档。 |
## 备注


当创建 [Table](../) 时，它属于指定的文档，但尚未成为文档的一部分，并且 [ParentNode](../../../aspose.words/node/get_parentnode/) 为 **null**。

要将 [Table](../) 追加到文档中，请在希望插入表格的故事上使用 [InsertAfter1()</see> 或 <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../)。

## 示例



展示如何创建表格。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// 表格包含行，行包含单元格，单元格可能包含段落
// 以及诸如运行、形状，甚至其他表格等典型元素。
// 在表格上调用 "EnsureMinimum" 方法将确保
// 表格至少有一个行、单元格和段落。
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// 向表格的第一行第一列单元格添加文本。
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```

## 另见

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
