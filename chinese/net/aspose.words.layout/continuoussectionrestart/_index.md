---
title: ContinuousSectionRestart Enum
linktitle: ContinuousSectionRestart
articleTitle: ContinuousSectionRestart
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Layout.ContinuousSectionRestart 枚举，获取连续部分中灵活的页码选项。轻松增强文档布局！
type: docs
weight: 3750
url: /zh/net/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enumeration

表示在重新开始页码编号的连续部分中计算页码时的不同行为。

```csharp
public enum ContinuousSectionRestart
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Always | `0` | 无论内容流如何，页码始终重新开始。 |
| FromNewPageOnly | `1` | 仅当章节开始页面上的章节之前没有其他内容时，页面编号才会重新开始。 |

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

* 命名空间 [Aspose.Words.Layout](../../aspose.words.layout/)
* 部件 [Aspose.Words](../../)
