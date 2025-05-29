---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
linktitle: ContinuousSectionPageNumberingRestart
articleTitle: ContinuousSectionPageNumberingRestart
second_title: Aspose.Words for .NET
description: 探索 LayoutOptions ContinuousSectionPageNumberingRestart 属性，实现连续部分页码的无缝控制。立即优化您的文档布局！
type: docs
weight: 40
url: /zh/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

获取或设置连续部分重新开始页码编号时计算页码的行为模式。

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

## 评论

默认值为Always . 它与 MS Word 2019 的行为相匹配，而 MS Word 2019 是引入该选项时的最新版本。 可以通过此选项使用 MS Word 2016 演示的旧页码编号逻辑。 请[`ContinuousSectionRestart`](../../continuoussectionrestart/)用于行为描述。

## 例子

展示如何控制连续部分中的页码。

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// 默认情况下，Aspose.Words 行为与 Microsoft Word 2019 匹配。
// 如果您需要旧的 Aspose.Words 行为，重复的 Microsoft Word 2016，请使用“ContinuousSectionRestart.FromNewPageOnly”。
// 仅当章节开始的页面上的章节之前没有其他内容时，页码才会重新开始，
// 因此从第二页开始编号将重置为 2。
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### 也可以看看

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* 命名空间 [Aspose.Words.Layout](../../../aspose.words.layout/)
* 部件 [Aspose.Words](../../../)
