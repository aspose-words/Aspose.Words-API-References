---
title: "Aspose::Words::Tables::Row::EnsureMinimum 方法"
linktitle: "EnsureMinimum"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Tables::Row::EnsureMinimum 方法。如果 Row 没有单元格，则在 C++ 中创建并追加一个 Cell。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.tables/row/ensureminimum/
---
## Row::EnsureMinimum method


如果 [Row](../) 没有单元格，则创建并追加一个 [Cell](../../cell/)。

```cpp
void Aspose::Words::Tables::Row::EnsureMinimum()
```


## 示例



展示如何确保行节点包含我们开始添加内容所需的节点。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// 行包含单元格，单元格中包含带有典型元素的段落，例如运行、形状，甚至其他表格。
// 我们的新行没有这些节点，且在拥有这些节点之前无法向其添加内容。
ASSERT_EQ(0, row->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// 在表格上调用 "EnsureMinimum" 方法将确保
// 表格至少有一个包含空段落的单元格。
row->EnsureMinimum();
row->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## 另见

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
