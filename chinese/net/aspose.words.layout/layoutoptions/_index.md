---
title: LayoutOptions Class
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Layout.LayoutOptions 来优化文档布局控制，通过灵活的自定义选项增强您的文字处理体验。
type: docs
weight: 3800
url: /zh/net/aspose.words.layout/layoutoptions/
---
## LayoutOptions class

包含允许控制文档布局过程的选项。

要了解更多信息，请访问[转换为固定页面格式](https://docs.aspose.com/words/net/converting-to-fixed-page-format/)文档文章。

```csharp
public class LayoutOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [LayoutOptions](layoutoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Callback](../../aspose.words.layout/layoutoptions/callback/) { get; set; } | 获取或设置[`IPageLayoutCallback`](../ipagelayoutcallback/)页面布局模型使用的实现。 |
| [CommentDisplayMode](../../aspose.words.layout/layoutoptions/commentdisplaymode/) { get; set; } | 获取或设置评论的呈现方式。 默认值为ShowInBalloons. |
| [ContinuousSectionPageNumberingRestart](../../aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/) { get; set; } | 获取或设置连续部分重新开始页码编号时计算页码的行为模式。 |
| [IgnorePrinterMetrics](../../aspose.words.layout/layoutoptions/ignoreprintermetrics/) { get; set; } | 获取或设置是否忽略“使用打印机指标来布局文档”兼容性选项的指示。 默认值为`真的`. |
| [KeepOriginalFontMetrics](../../aspose.words.layout/layoutoptions/keeporiginalfontmetrics/) { get; set; } | 获取或设置字体替换后是否应使用原始字体规格的指示。 默认值为`真的`. |
| [RevisionOptions](../../aspose.words.layout/layoutoptions/revisionoptions/) { get; } | 获取修订选项。 |
| [ShowHiddenText](../../aspose.words.layout/layoutoptions/showhiddentext/) { get; set; } | 获取或设置是否显示文档中隐藏文本的指示。 默认值为`错误的`. |
| [ShowParagraphMarks](../../aspose.words.layout/layoutoptions/showparagraphmarks/) { get; set; } | 获取或设置是否呈现段落标记的指示。 默认值为`错误的`. |
| [TextShaperFactory](../../aspose.words.layout/layoutoptions/textshaperfactory/) { get; set; } | 获取或设置[`ITextShaperFactory`](../../aspose.words.shaping/itextshaperfactory/)用于高级排版渲染功能的实现。 |

## 评论

您不能直接创建此类的实例。使用[`LayoutOptions`](../../aspose.words/document/layoutoptions/)属性来访问此文档的布局选项。

请注意，在更改此类中的任何选项后，[`UpdatePageLayout`](../../aspose.words/document/updatepagelayout/)应该调用 method 以便将更改的选项应用到布局。

## 例子

展示如何在渲染的输出文档中隐藏文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// 插入隐藏文本，然后指定我们是否希望从呈现的文档中省略它。
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

展示如何在渲染的输出文档中显示段落标记。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// 添加一些段落，然后启用段落标记来显示段落的结尾
// 当我们呈现文档时，使用段落标记 (¶) 符号。
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

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
