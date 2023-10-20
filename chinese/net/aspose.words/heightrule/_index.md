---
title: HeightRule Enum
linktitle: HeightRule
articleTitle: HeightRule
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.HeightRule 枚举. 指定确定对象高度的规则 在 C#.
type: docs
weight: 3130
url: /zh/net/aspose.words/heightrule/
---
## HeightRule enumeration

指定确定对象高度的规则。

```csharp
public enum HeightRule
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| AtLeast | `0` | 高度将至少为指定高度（以磅为单位）。如果需要，它将增长 以容纳对象内的所有文本。 |
| Exactly | `1` | 高度以磅为单位精确指定。请注意，如果文本无法 放入此高度的对象内，它将显示为被截断。 |
| Auto | `2` | 高度将自动增长以容纳对象内的所有文本。 |

## 例子

演示如何使用文档生成器设置行格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// 开始第二行，然后配置其高度。构建器会将这些设置应用到
// 它的当前行，以及之后创建的任何新行。
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// 第一行不受填充重新配置的影响，仍然保留默认值。
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
