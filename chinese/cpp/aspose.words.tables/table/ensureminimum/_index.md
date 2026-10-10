---
title: "Aspose::Words::Tables::Table::EnsureMinimum 方法"
linktitle: "EnsureMinimum"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Table::EnsureMinimum 方法。如果表没有行，则在 C++ 中创建并追加一行 Row。"
type: docs
weight: 8000
url: /zh/cpp/aspose.words.tables/table/ensureminimum/
---
## Table::EnsureMinimum method


如果表没有行，则创建并追加一个 [Row](../../row/)。

```cpp
void Aspose::Words::Tables::Table::EnsureMinimum()
```


## 示例



展示如何确保表节点包含我们添加内容所需的节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// 表包含行，行包含单元格，单元格可能包含段落
// 以及诸如运行、形状，甚至其他表格等典型元素。
// 我们的新表没有这些节点，在它拥有这些节点之前我们无法向其添加内容。
ASSERT_EQ(0, table->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// 在表格上调用 "EnsureMinimum" 方法将确保
// 表至少有一行和一个包含空段落的单元格。
table->EnsureMinimum();
table->get_FirstRow()->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## 另见

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
