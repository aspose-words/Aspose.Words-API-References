---
title: HeightRule Enum
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.HeightRule 枚举，精确控制文档中对象的高度。使用这项重要功能优化您的工作流程！
type: docs
weight: 3560
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
| AtLeast | `0` | 高度至少为指定的点数高度。如有需要，高度将增大， 以容纳对象内的所有文本。 |
| Exactly | `1` | 高度以磅为单位精确指定。请注意，如果文本无法 容纳在此高度的对象内，则会显示为截断。 |
| Auto | `2` | 高度将自动增加以容纳对象内的所有文本。 |

## 例子

展示如何使用文档生成器来格式化行。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// 开始第二行，然后配置其高度。构建器将应用这些设置到
// 它的当前行，以及它之后创建的任何新行。
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
