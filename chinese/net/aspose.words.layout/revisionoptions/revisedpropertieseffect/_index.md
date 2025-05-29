---
title: RevisionOptions.RevisedPropertiesEffect
linktitle: RevisedPropertiesEffect
articleTitle: RevisedPropertiesEffect
second_title: Aspose.Words for .NET
description: 了解 RevisionOptions 中的 RevisedPropertiesEffect 如何增强您的内容格式。使用 FormatChange 功能轻松自定义更改。
type: docs
weight: 140
url: /zh/net/aspose.words.layout/revisionoptions/revisedpropertieseffect/
---
## RevisionOptions.RevisedPropertiesEffect property

允许指定格式属性变化的内容区域的效果FormatChange 默认值为None

```csharp
public RevisionTextEffect RevisedPropertiesEffect { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentOutOfRangeException | Hidden是不允许的。 |

## 例子

展示如何修改修订的外观。

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// 获取控制修订外观的 RevisionOptions 对象。
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// 以绿色和斜体呈现插入修订。
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// 以红色和粗体呈现删除修订。
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// 相同的文本将在动作修订中出现两次：
// 一次在出发点，一次在到达目的地。
// 将移出修订版的文本渲染为黄色，并带有双删除线
// 并在移至的修订版处使用双下划线蓝色。
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedToTextEffect = RevisionTextEffect.DoubleUnderline;

// 以深红色和粗体呈现格式修订。
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// 在页面左侧受修订影响的行旁边放置一个粗深蓝色条。
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// 显示修订标记和原始文本。
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// 使移动、删除、格式修改和评论显示在绿色气球中
// 在页面的右侧。
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// 这些功能仅适用于.pdf或.jpg等格式。
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### 也可以看看

* enum [RevisionTextEffect](../../revisiontexteffect/)
* class [RevisionOptions](../)
* 命名空间 [Aspose.Words.Layout](../../../aspose.words.layout/)
* 部件 [Aspose.Words](../../../)
