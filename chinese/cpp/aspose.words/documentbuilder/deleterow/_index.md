---
title: "Aspose::Words::DocumentBuilder::DeleteRow 方法"
linktitle: "DeleteRow"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBuilder::DeleteRow 方法。删除 C++ 中表格的一行。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder::DeleteRow method


删除表中的一行。

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::DocumentBuilder::DeleteRow(int32_t tableIndex, int32_t rowIndex)
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| tableIndex | int32_t | 表格的索引。 |
| rowIndex | int32_t | 表格中行的索引。 |

### ReturnValue

刚刚被移除的行节点。
## 备注


如果光标位于正在删除的行内，光标将移动到下一行或表格后的下一段落。

如果从仅包含一行的表格中删除该行，整个表格将被删除。

对于索引参数，当 index 大于或等于 0 时，它表示从开头开始的索引，0 为第一个元素。当 index 小于 0 时，它表示从末尾算起的索引，-1 为最后一个元素。

## 示例



展示如何从表格中删除一行。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, cell 2.");
builder->EndTable();

ASSERT_EQ(2, table->get_Rows()->get_Count());

// 删除文档中第一个表格的第一行。
builder->DeleteRow(0, 0);

ASSERT_EQ(1, table->get_Rows()->get_Count());
ASSERT_EQ(u"Row 2, cell 1.\aRow 2, cell 2.\a\a", table->GetText().Trim());
```

## 另见

* Class [Row](../../../aspose.words.tables/row/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
