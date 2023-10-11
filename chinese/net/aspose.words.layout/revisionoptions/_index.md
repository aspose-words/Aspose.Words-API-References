---
title: Class RevisionOptions
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Layout.RevisionOptions 班级. 允许控制在布局过程中如何处理文档修订
type: docs
weight: 3390
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
| [CommentColor](../../aspose.words.layout/revisionoptions/commentcolor/) { get; set; } | 允许指定用于注释的颜色。 默认值为Red. |
| [DeletedTextColor](../../aspose.words.layout/revisionoptions/deletedtextcolor/) { get; set; } | 允许指定用于删除内容的颜色Deletion. 默认值为ByAuthor. |
| [DeletedTextEffect](../../aspose.words.layout/revisionoptions/deletedtexteffect/) { get; set; } | 允许指定要应用于已删除内容的效果Deletion. 默认值为StrikeThrough |
| [InsertedTextColor](../../aspose.words.layout/revisionoptions/insertedtextcolor/) { get; set; } | 允许指定用于插入内容的颜色Insertion. 默认值为ByAuthor. |
| [InsertedTextEffect](../../aspose.words.layout/revisionoptions/insertedtexteffect/) { get; set; } | 允许指定要应用于插入内容的效果Insertion. 默认值为Underline. |
| [MeasurementUnit](../../aspose.words.layout/revisionoptions/measurementunit/) { get; set; } | 允许指定修订注释的测量单位。 默认值为Centimeters |
| [MovedFromTextColor](../../aspose.words.layout/revisionoptions/movedfromtextcolor/) { get; set; } | 允许指定用于移动内容的区域的颜色Moving. 默认值为ByAuthor. |
| [MovedFromTextEffect](../../aspose.words.layout/revisionoptions/movedfromtexteffect/) { get; set; } | 允许指定应用于内容移出区域的效果Moving. 默认值为DoubleStrikeThrough |
| [MovedToTextColor](../../aspose.words.layout/revisionoptions/movedtotextcolor/) { get; set; } | 允许指定内容移动到的区域使用的颜色Moving. 默认值为ByAuthor. |
| [MovedToTextEffect](../../aspose.words.layout/revisionoptions/movedtotexteffect/) { get; set; } | 允许指定要应用于内容移动到的区域的效果Moving. 默认值为DoubleUnderline |
| [RevisedPropertiesColor](../../aspose.words.layout/revisionoptions/revisedpropertiescolor/) { get; set; } | 允许指定用于更改格式属性的内容的颜色FormatChange 默认值为NoHighlight. |
| [RevisedPropertiesEffect](../../aspose.words.layout/revisionoptions/revisedpropertieseffect/) { get; set; } | 允许通过更改格式属性来指定内容区域的效果FormatChange 默认值为None |
| [RevisionBarsColor](../../aspose.words.layout/revisionoptions/revisionbarscolor/) { get; set; } | 允许指定用于标识包含修订信息的文档行的侧边栏的颜色。 默认值为Red. |
| [RevisionBarsPosition](../../aspose.words.layout/revisionoptions/revisionbarsposition/) { get; set; } | 获取或设置修订栏的渲染位置。 默认值为Outside. |
| [RevisionBarsWidth](../../aspose.words.layout/revisionoptions/revisionbarswidth/) { get; set; } | 获取或设置修订栏的宽度、点。 |
| [ShowInBalloons](../../aspose.words.layout/revisionoptions/showinballoons/) { get; set; } | 允许指定修订是否在气球中呈现。 默认值为None. |
| [ShowOriginalRevision](../../aspose.words.layout/revisionoptions/showoriginalrevision/) { get; set; } | 允许指定是否应显示原始文本而不是修订后的文本。 默认值为`错误的`. |
| [ShowRevisionBars](../../aspose.words.layout/revisionoptions/showrevisionbars/) { get; set; } | 允许指定是否应在包含修订内容的行附近呈现修订栏。 默认值为`真的`. |
| [ShowRevisionMarks](../../aspose.words.layout/revisionoptions/showrevisionmarks/) { get; set; } | 允许指定是否应使用特殊格式标记来标记修订文本。 默认值为`真的`. |

### 例子

演示如何更改渲染输出文档中修订的外观。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入一个修订版本，然后将所有修订版本的颜色更改为绿色。
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// 删除出现在每条修改行左侧的栏。
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### 也可以看看

* 命名空间 [Aspose.Words.Layout](../../aspose.words.layout/)
* 部件 [Aspose.Words](../../)


