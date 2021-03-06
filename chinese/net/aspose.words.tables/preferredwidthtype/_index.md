---
title: PreferredWidthType
second_title: Aspose.Words for .NET API 参考
description: 指定表格或单元格的首选宽度的度量单位
type: docs
weight: 6000
url: /zh/net/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enumeration

指定表格或单元格的首选宽度的度量单位。

```csharp
public enum PreferredWidthType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Auto | `1` | 未指定首选宽度。表格或单元格的实际宽度要么使用显式宽度指定，要么 将在表格显示时由表格布局算法自动确定，具体取决于表格自动调整设置。 |
| Percent | `2` | 使用指定百分比测量当前项目宽度。 |
| Points | `3` | 使用指定的点数（1/72 英寸）测量当前项目宽度。 |

### 例子

显示如何验证表格单元格的首选宽度类型和值。

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### 也可以看看

* class [PreferredWidth](../preferredwidth)
* 命名空间 [Aspose.Words.Tables](../../aspose.words.tables)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
