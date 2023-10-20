---
title: TextColumnCollection.SetCount
linktitle: SetCount
articleTitle: SetCount
second_title: 用于 .NET 的 Aspose.Words
description: TextColumnCollection SetCount 方法. 将文本排列到指定数量的文本列中 在 C#.
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

什么时候[`EvenlySpaced`](../evenlyspaced/)是`错误的`然后您增加列数， new[`TextColumn`](../../textcolumn/)创建的对象的宽度和间距为零。 您需要为新列设置宽度和间距。

## 例子

演示如何在一个部分中创建多个均匀间隔的列。

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
