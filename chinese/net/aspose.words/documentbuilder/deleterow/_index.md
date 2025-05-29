---
title: DocumentBuilder.DeleteRow
linktitle: DeleteRow
articleTitle: DeleteRow
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder 的 DeleteRow 方法轻松从表格中删除行。简化您的文档编辑并增强您的工作流程！
type: docs
weight: 200
url: /zh/net/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder.DeleteRow method

从表中删除一行。

```csharp
public Row DeleteRow(int tableIndex, int rowIndex)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| tableIndex | Int32 | 表的索引。 |
| rowIndex | Int32 | 表中行的索引。 |

### 返回值

刚刚删除的行节点。

## 评论

如果光标位于要删除的行内，则光标将移动至下一行或表格后的下一个段落。

如果从仅包含一行的表中删除一行，则会删除整个 表。

对于 index 参数，当 index 大于等于 0 时，指定从 开始的索引，0 为第一个元素。当 index 小于 0 时，指定从 结束的索引，-1 为最后一个元素。

## 例子

展示如何从表中删除一行。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();
builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.Write("Row 2, cell 2.");
builder.EndTable();

Assert.AreEqual(2, table.Rows.Count);

// 删除文档中第一个表格的第一行。
builder.DeleteRow(0, 0);

Assert.AreEqual(1, table.Rows.Count);
Assert.AreEqual("Row 2, cell 1.\aRow 2, cell 2.\a\a", table.GetText().Trim());
```

### 也可以看看

* class [Row](../../../aspose.words.tables/row/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
