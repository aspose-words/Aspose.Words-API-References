---
title: Enum ShowInBalloons
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Layout.ShowInBalloons 枚举. 指定在气球中呈现的修订版本
type: docs
weight: 3210
url: /zh/net/aspose.words.layout/showinballoons/
---
## ShowInBalloons enumeration

指定在气球中呈现的修订版本。

```csharp
public enum ShowInBalloons
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 呈现插入、删除和格式化内联修订。 |
| Format | `1` | 呈现插入和删除内联修订，在气球中格式化修订。 |
| FormatAndDelete | `2` | 在气球中呈现插入修订、删除和格式化修订。 |

### 评论

请注意，修订不会在气球中呈现ShowInAnnotations.

### 例子

显示如何修改修订的外观。

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

// 相同的文本将在一次移动修订中出现两次：
// 一次在出发点，一次在到达目的地。
// 将移出修订版处的文本渲染为黄色，并带有双删除线
// 并在移至的修订版处加双下划线蓝色。
revisionOptions.MovedFromTextColor = RevisionColor.Yellow;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.MovedToTextColor = RevisionColor.Blue;
revisionOptions.MovedFromTextEffect = RevisionTextEffect.DoubleUnderline;

// 以深红色和粗体呈现格式修订。
revisionOptions.RevisedPropertiesColor = RevisionColor.DarkRed;
revisionOptions.RevisedPropertiesEffect = RevisionTextEffect.Bold;

// 在页面左侧受修订影响的行旁边放置一个深蓝色粗条。
revisionOptions.RevisionBarsColor = RevisionColor.DarkBlue;
revisionOptions.RevisionBarsWidth = 15.0f;

// 显示修订标记和原始文本。
revisionOptions.ShowOriginalRevision = true;
revisionOptions.ShowRevisionMarks = true;

// 获取移动、删除、格式化修订和评论以显示在绿色气球中
// 在页面的右侧。
revisionOptions.ShowInBalloons = ShowInBalloons.Format;
revisionOptions.CommentColor = RevisionColor.BrightGreen;

// 这些特性仅适用于 .pdf 或 .jpg 等格式。
doc.Save(ArtifactsDir + "Revision.RevisionOptions.pdf");
```

### 也可以看看

* 命名空间 [Aspose.Words.Layout](../../aspose.words.layout/)
* 部件 [Aspose.Words](../../)


