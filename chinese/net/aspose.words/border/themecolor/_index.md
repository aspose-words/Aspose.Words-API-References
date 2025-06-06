---
title: Border.ThemeColor
linktitle: ThemeColor
articleTitle: ThemeColor
second_title: Aspose.Words for .NET
description: 了解如何使用 Border ThemeColor 属性自定义您的配色方案并使用充满活力的定制主题增强您的设计。
type: docs
weight: 70
url: /zh/net/aspose.words/border/themecolor/
---
## Border.ThemeColor property

获取或设置与此 Border 对象关联的应用配色方案中的主题颜色。

```csharp
public ThemeColor ThemeColor { get; set; }
```

## 例子

演示如何插入带有顶部边框的段落。

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
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
