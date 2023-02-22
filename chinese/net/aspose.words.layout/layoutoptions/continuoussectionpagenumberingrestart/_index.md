---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
second_title: Aspose.Words for .NET API 参考
description: LayoutOptions 财产. 获取或设置在连续节 重新开始页码时计算页码的行为模式
type: docs
weight: 40
url: /zh/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

获取或设置在连续节 重新开始页码时计算页码的行为模式。

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

### 评论

默认值为Always . 它与 MS Word 2019 的行为相匹配，这是引入该选项时的最新版本。 MS Word 2016 演示的旧页码逻辑可通过此选项获得。 请[`ContinuousSectionRestart`](../../continuoussectionrestart/)对于行为描述。

### 例子

显示如何控制连续部分中的页码。

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// 默认情况下，Aspose.Words 行为与 Microsoft Word 2019 匹配。
// 如果您需要旧的 Aspose.Words 行为，重复 Microsoft Word 2016，请使用“ContinuousSectionRestart.FromNewPageOnly”。
// 只有在节开始的页面上的节之前没有其他内容时，才重新开始页码，
//因此编号将从第二页重置为2。
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### 也可以看看

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* 命名空间 [Aspose.Words.Layout](../../layoutoptions/)
* 部件 [Aspose.Words](../../../)


