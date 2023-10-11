---
title: Border.ThemeColor
second_title: Aspose.Words for .NET API 参考
description: Border 财产. 获取或设置与此 Border 对象关联的已应用配色方案中的主题颜色
type: docs
weight: 70
url: /zh/net/aspose.words/border/themecolor/
---
## Border.ThemeColor property

获取或设置与此 Border 对象关联的已应用配色方案中的主题颜色。

```csharp
public ThemeColor ThemeColor { get; set; }
```

### 例子

演示如何插入带有上边框的段落。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// 仅当设置了 LineWidth 或 LineStyle 时才设置 ThemeColor。
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### 也可以看看

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Border](../)
* 命名空间 [Aspose.Words](../../border/)
* 部件 [Aspose.Words](../../../)


