---
title: RevisionOptions Class
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Layout.RevisionOptions 类以有效管理文档修订并增强布局流程以获得最佳结果。
type: docs
weight: 3840
url: /zh/net/aspose.words.layout/revisionoptions/
---
## RevisionOptions class

允许控制在布局过程中如何处理文档修订。

要了解更多信息，请访问[转换为固定页面格式](https://docs.aspose.com/words/net/converting-to-fixed-page-format/)文档文章。

```csharp
public class RevisionOptions
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | 允许指定用于评论的颜色。 默认值为Red. |
| [DeleteCellColor](../../aspose.words.layout/revisionoptions/deletecellcolor/) { get; set; } | 允许指定已删除单元格所使用的颜色Deletion. 默认值是Pink. |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | 允许指定已删除内容所使用的颜色Deletion. 默认值是ByAuthor. |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | 允许指定应用于已删除内容的效果Deletion. 默认值是StrikeThrough |
| [InsertCellColor](../../aspose.words.layout/revisionoptions/insertcellcolor/) { get; set; } | 允许指定插入单元格使用的颜色Insertion. 默认值是Blue. |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | 允许指定插入内容所使用的颜色Insertion. 默认值是ByAuthor. |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | 允许指定应用于插入内容的效果Insertion. 默认值是Underline. |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | 允许指定修订注释的测量单位。 默认值为Centimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | 允许指定内容从哪里移动的区域使用的颜色Moving. 默认值是ByAuthor. |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | 允许指定应用于内容移动区域的效果Moving. 默认值是DoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | 允许指定内容移动到的区域所使用的颜色Moving. 默认值是ByAuthor. |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | 允许指定应用于内容移动到的区域的效果Moving. 默认值是DoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | 允许指定用于更改格式属性的内容的颜色FormatChange 默认值为NoHighlight. |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | 允许指定格式属性变化的内容区域的效果FormatChange 默认值为None |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | 允许指定用于标识包含修订信息的文档行的侧边栏的颜色。 默认值为Red. |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | 获取或设置修订栏的渲染位置。 默认值为Outside. |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | 获取或设置修订栏的宽度，单位为点。 |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | 允许指定修订是否在气球中呈现。 默认值为None. |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | 允许指定是否显示原始文本而不是修订文本。 默认值为`错误的`. |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | 允许指定修订栏是否应在包含修订内容的行附近呈现。 默认值为`真的`. |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | 允许指定修订文本是否应使用特殊格式标记。 默认值为`真的`. |

## 例子

展示如何改变渲染输出文档中修订版本的外观。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入修订，然后将所有修订的颜色更改为绿色。
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// 删除出现在每个修订行左侧的栏。
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### 也可以看看

* 命名空间 [Aspose.Words.Layout](../../aspose.words.layout/)
* 部件 [Aspose.Words](../../)
