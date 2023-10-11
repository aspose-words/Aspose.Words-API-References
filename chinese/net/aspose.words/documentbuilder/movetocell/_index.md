---
title: DocumentBuilder.MoveToCell
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 方法. 将光标移动到当前部分中的表格单元格
type: docs
weight: 510
url: /zh/net/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder.MoveToCell method

将光标移动到当前部分中的表格单元格。

```csharp
public void MoveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| tableIndex | Int32 | 要移动到的表的索引。 |
| rowIndex | Int32 | 表中行的索引。 |
| columnIndex | Int32 | 表中列的索引。 |
| characterIndex | Int32 | 单元格内字符的索引。 负值允许您指定从单元格末尾开始的位置。使用 -1 移动到单元格的末尾 of 。 |

### 评论

导航在当前部分的当前故事内执行。

对于索引参数，当index大于或等于0时，指定索引从 开始，以0为第一个元素。当index小于0时，它指定一个索引from 结尾，-1是最后一个元素。

### 例子

演示如何将文档生成器的光标移动到表中的单元格。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个空的 2x2 表。
builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

// 因为我们已经用 EndTable 方法结束了表格，
// 文档构建器的光标当前位于表格之外。
// 该光标与 Microsoft Word 的闪烁文本光标具有相同的功能。
// 还可以使用构建器的 MoveTo 方法将其移动到文档中的其他位置。
// 我们可以将光标移回表格内的特定单元格。
builder.MoveToCell(0, 1, 1, 0);
builder.Write("Column 2, cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.MoveToCell.docx");
```

### 也可以看看

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


