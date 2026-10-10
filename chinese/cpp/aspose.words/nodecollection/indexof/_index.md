---
title: "Aspose::Words::NodeCollection::IndexOf 方法"
linktitle: "IndexOf"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::NodeCollection::IndexOf 方法。返回在 C++ 中指定节点的从零开始的索引。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words/nodecollection/indexof/
---
## NodeCollection::IndexOf method


返回指定节点的从零开始的索引。

```cpp
int32_t Aspose::Words::NodeCollection::IndexOf(const System::SharedPtr<Aspose::Words::Node> &node)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| 节点 | const System::SharedPtr\<Aspose::Words::Node\>\& | 要定位的节点。 |

### ReturnValue

如果找到，则返回集合中节点的从零开始的索引；否则为 -1。
## 备注


此方法执行线性搜索；因此，平均执行时间与 [Count](../get_count/) 成正比。

## 示例



展示如何获取集合中节点的索引。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::NodeCollection> allTables = doc->GetChildNodes(Aspose::Words::NodeType::Table, true);

ASSERT_EQ(0, allTables->IndexOf(table));

System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(2);

ASSERT_EQ(2, table->IndexOf(row));

System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_LastCell();

ASSERT_EQ(4, row->IndexOf(cell));
```

## 另见

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
