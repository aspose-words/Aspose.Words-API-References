---
title: Style.Priority
linktitle: Priority
articleTitle: Priority
second_title: Aspose.Words for .NET
description: 了解如何管理样式优先级设置，以优化任务窗格中的样式排序。通过高效的样式组织，提升您的工作流程！
type: docs
weight: 160
url: /zh/net/aspose.words/style/priority/
---
## Style.Priority property

获取/设置表示在“样式”任务窗格中对样式进行排序的优先级的整数值。

```csharp
public int Priority { get; set; }
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
