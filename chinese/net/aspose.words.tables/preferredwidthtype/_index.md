---
title: PreferredWidthType Enum
linktitle: PreferredWidthType
articleTitle: PreferredWidthType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Tables.PreferredWidthType 枚举。轻松定义表格和单元格的宽度测量值，实现精确的文档格式。
type: docs
weight: 7150
url: /zh/net/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enumeration

指定表格或单元格的首选宽度的测量单位。

```csharp
public enum PreferredWidthType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Auto | `1` | 未指定首选宽度。表格或单元格的实际宽度可以使用显式宽度指定，或 将在表格显示时由表格布局算法自动确定，具体取决于表格的自动调整设置。 |
| Percent | `2` | 使用指定的百分比测量当前项目宽度。 |
| Points | `3` | 使用指定数量的点（1/72 英寸）测量当前项目宽度。 |

## 例子

展示如何验证表格单元格的首选宽度类型和值。

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### 也可以看看

* class [PreferredWidth](../preferredwidth/)
* 命名空间 [Aspose.Words.Tables](../../aspose.words.tables/)
* 部件 [Aspose.Words](../../)
