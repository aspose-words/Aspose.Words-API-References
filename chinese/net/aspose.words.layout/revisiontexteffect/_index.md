---
title: RevisionTextEffect Enum
linktitle: RevisionTextEffect
articleTitle: RevisionTextEffect
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Layout.RevisionTextEffect 枚举，使用独特的文本修饰效果增强文档修订功能。提升您的编辑体验！
type: docs
weight: 3850
url: /zh/net/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enumeration

允许指定文档文本修订的装饰效果。

```csharp
public enum RevisionTextEffect
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 修订内容未应用任何特殊效果。 这对应于NoHighlight. |
| Color | `1` | 修订内容仅以颜色突出显示。 |
| Bold | `2` | 修订后的内容以粗体和彩色显示。 |
| Italic | `3` | 修订后的内容以斜体和彩色显示。 |
| Underline | `4` | 修订内容带有下划线和颜色。 |
| DoubleUnderline | `5` | 修订内容带有双下划线和彩色。 |
| StrikeThrough | `6` | 修改后的内容被划掉并着色。 |
| DoubleStrikeThrough | `7` | 修订内容被双击并着色。 |
| Hidden | `8` | 修订内容已隐藏。 |

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

* 命名空间 [Aspose.Words.Layout](../../aspose.words.layout/)
* 部件 [Aspose.Words](../../)
