---
title: CellFormat.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words for .NET
description: 探索 CellFormat ClearFormatting 方法，轻松将单元格样式重置为默认值，且不改变单元格宽度。提升您的电子表格效率！
type: docs
weight: 160
url: /zh/net/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat.ClearFormatting method

重置为默认单元格格式。不改变单元格宽度。

```csharp
public void ClearFormatting()
```

## 例子

展示如何将两个表中的行合并为一个。

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// 以下是从文档中获取表格的两种方法。
// 1 - 来自 Body 节点的“Tables”集合：
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - 使用“GetChild”方法：
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// 将当前表中的所有行附加到下一个表。
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// 删除空的表格容器。
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### 也可以看看

* class [CellFormat](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
