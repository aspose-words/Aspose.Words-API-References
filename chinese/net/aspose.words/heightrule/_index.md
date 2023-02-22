---
title: Enum HeightRule
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.HeightRule 枚举. 指定确定对象高度的规则
type: docs
weight: 2950
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
| AtLeast | `0` | 高度至少为指定的高度（以磅为单位）。如果需要，它将增长， 以容纳对象内的所有文本。 |
| Exactly | `1` | 高度以磅为单位精确指定。请注意，如果文本不能 适合此高度的对象，则会出现截断。 |
| Auto | `2` | 高度将自动增加以容纳对象内的所有文本。 |

### 例子

显示如何使用文档构建器格式化行。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// 开始第二行，然后配置它的高度。构建器会将这些设置应用于
// 它的当前行，以及它之后创建的任何新行。
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// 第一行不受填充重新配置的影响，仍然保持默认值。
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


