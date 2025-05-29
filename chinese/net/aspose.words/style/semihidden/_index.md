---
title: Style.SemiHidden
linktitle: SemiHidden
articleTitle: SemiHidden
second_title: Aspose.Words for .NET
description: 了解 SemiHidden 属性如何控制样式库和任务窗格中的样式可见性，从而增强您的设计工作流程和效率。
type: docs
weight: 170
url: /zh/net/aspose.words/style/semihidden/
---
## Style.SemiHidden property

获取/设置样式是否从样式库和样式任务窗格中隐藏。

```csharp
public bool SemiHidden { get; set; }
```

## 例子

展示如何确定样式的优先级以及隐藏样式。

```csharp
Document doc = new Document();
Style styleTitle = doc.Styles[StyleIdentifier.Subtitle];

if (styleTitle.Priority == 9)
    styleTitle.Priority = 10;

if (!styleTitle.UnhideWhenUsed)
    styleTitle.UnhideWhenUsed = true;

if (styleTitle.SemiHidden)
    styleTitle.SemiHidden = true;

doc.Save(ArtifactsDir + "Styles.StylePriority.docx");
```

### 也可以看看

* class [Style](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
