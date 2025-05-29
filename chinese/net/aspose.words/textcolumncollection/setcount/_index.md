---
title: TextColumnCollection.SetCount
linktitle: SetCount
articleTitle: SetCount
second_title: Aspose.Words for .NET
description: 使用 TextColumnCollection SetCount 方法优化您的布局，轻松地将文本排列到所需的列数中，以增强可读性。
type: docs
weight: 70
url: /zh/net/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection.SetCount method

将文本排列到指定数量的文本列中。

```csharp
public void SetCount(int newCount)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| newCount | Int32 | 文本要排列成的列数。 |

## 评论

什么时候[`EvenlySpaced`](../evenlyspaced/)是`错误的`并增加列数， new[`TextColumn`](../../textcolumn/)对象以零宽度和间距创建。 您需要为新列设置宽度和间距。

## 例子

展示如何在一个部分中创建多个间距均匀的列。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### 也可以看看

* class [TextColumnCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
