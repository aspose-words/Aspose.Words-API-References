---
title: DocumentBuilder.DeleteRow
linktitle: DeleteRow
articleTitle: DeleteRow
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder DeleteRow 方法. 从表中删除一行 在 C#.
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

如果光标位于要删除的行内部，则光标将移出 到下一行或表后的下一个段落。

如果从仅包含一行的表中删除一行，则 Whole 表将被删除。

对于索引参数，当index大于或等于0时，指定索引从 开始，以0为第一个元素。当index小于0时，它指定一个索引from 结尾，-1是最后一个元素。

## 例子

演示如何从表中删除行。

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
