---
title: "Aspose::Words::Tables::Cell::EnsureMinimum 方法"
linktitle: "EnsureMinimum"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Cell::EnsureMinimum 方法。如果最后一个子节点不是段落，则在 C++ 中创建并追加一个空段落。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.tables/cell/ensureminimum/
---
## Cell::EnsureMinimum method


如果最后一个子节点不是段落，则创建并追加一个空段落。

```cpp
void Aspose::Words::Tables::Cell::EnsureMinimum()
```


## 示例



展示如何确保单元格节点包含我们开始添加内容所需的节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);
auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

// 单元格可能包含带有常见元素（如运行、形状，甚至其他表格）的段落。
// 我们的新单元格没有任何段落，在此之前我们无法向其添加如 run 和 shape 节点等内容。
ASSERT_EQ(0, cell->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// 对单元格调用 "EnsureMinimum" 方法将确保
// 该单元格至少有一个空段落，我们随后可以向其添加内容。
cell->EnsureMinimum();
cell->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## 另见

* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
