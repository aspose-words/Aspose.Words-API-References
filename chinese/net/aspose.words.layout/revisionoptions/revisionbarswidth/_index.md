---
title: RevisionOptions.RevisionBarsWidth
second_title: Aspose.Words for .NET API 参考
description: RevisionOptions 财产. 获取或设置修订栏的宽度点
type: docs
weight: 150
url: /zh/net/aspose.words.layout/revisionoptions/revisionbarswidth/
---
## RevisionOptions.RevisionBarsWidth property

获取或设置修订栏的宽度、点。

```csharp
public float RevisionBarsWidth { get; set; }
```

### 例子

展示如何修改修订版本的外观。

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// 获取控制修订外观的 RevisionOptions 对象。
RevisionOptions revisionOptions = doc.LayoutOptions.RevisionOptions;

// 以绿色和斜体渲染插入修订。
revisionOptions.InsertedTextColor = RevisionColor.Green;
revisionOptions.InsertedTextEffect = RevisionTextEffect.Italic;

// 以红色和粗体呈现删除修订。
revisionOptions.DeletedTextColor = RevisionColor.Red;
revisionOptions.DeletedTextEffect = RevisionTextEffect.Bold;

// 相同的文本将在运动修订中出现两次：
// 一次在出发点，一次在到达目的地。
// 将移出的修订版本处的文本渲染为黄色，并带有双删除线
// 并在移至的修订版处显示蓝色双下划线。
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.ClassicBlue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// 以深红色和粗体渲染格式修订版。
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// 在页面左侧受修订影响的行旁边放置一个粗的深蓝色条。
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// 显示修订标记和原始文本。
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// 获取移动、删除、格式修订和注释以显示在绿色气球中
// 在页面的右侧。
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// 这些功能仅适用于 .pdf 或 .jpg 等格式。
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### 也可以看看

* class [RevisionOptions](../)
* 命名空间 [Aspose.Words.Layout](../../revisionoptions/)
* 部件 [Aspose.Words](../../../)


