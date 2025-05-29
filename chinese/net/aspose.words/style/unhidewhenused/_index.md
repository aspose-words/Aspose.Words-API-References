---
title: Style.UnhideWhenUsed
linktitle: UnhideWhenUsed
articleTitle: UnhideWhenUsed
second_title: Aspose.Words for .NET
description: 了解如何管理样式的 UnhideWhenUsed 属性。控制样式库和任务窗格中的可见性，以增强文档的设计效果。
type: docs
weight: 210
url: /zh/net/aspose.words/style/unhidewhenused/
---
## Style.UnhideWhenUsed property

获取/设置当前文档中使用的样式是否从样式库和样式任务窗格中取消隐藏。 当使用的样式应显示在样式库中时为 True。

```csharp
public bool UnhideWhenUsed { get; set; }
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
