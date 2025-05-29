---
title: RevisionOptions.DeleteCellColor
linktitle: DeleteCellColor
articleTitle: DeleteCellColor
second_title: Aspose.Words for .NET
description: 使用 RevisionOptions 的 DeleteCellColor 属性自定义您的电子表格。轻松为已删除的单元格设置独特的颜色，增强清晰度和条理性。
type: docs
weight: 20
url: /zh/net/aspose.words.layout/revisionoptions/deletecellcolor/
---
## RevisionOptions.DeleteCellColor property

允许指定已删除单元格所使用的颜色Deletion. 默认值是Pink.

```csharp
public RevisionColor DeleteCellColor { get; set; }
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
