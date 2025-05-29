---
title: RevisionOptions.InsertCellColor
linktitle: InsertCellColor
articleTitle: InsertCellColor
second_title: Aspose.Words for .NET
description: 使用 RevisionOptions 中的 InsertCellColor 属性自定义您的电子表格。选择您喜欢的插入单元格颜色——默认为蓝色！
type: docs
weight: 50
url: /zh/net/aspose.words.layout/revisionoptions/insertcellcolor/
---
## RevisionOptions.InsertCellColor property

允许指定插入单元格使用的颜色Insertion. 默认值是Blue.

```csharp
public RevisionColor InsertCellColor { get; set; }
```

## 例子

展示如何使用插入/删除单元格修订颜色。

```csharp
Document doc = new Document(MyDir + "Cell revisions.docx");

doc.LayoutOptions.RevisionOptions.InsertCellColor = RevisionColor.LightBlue;
doc.LayoutOptions.RevisionOptions.DeleteCellColor = RevisionColor.DarkRed;

doc.Save(ArtifactsDir + "Revision.RevisionCellColor.pdf");
```

### 也可以看看

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* 命名空间 [Aspose.Words.Layout](../../../aspose.words.layout/)
* 部件 [Aspose.Words](../../../)
