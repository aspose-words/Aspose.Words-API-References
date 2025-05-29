---
title: ParagraphFormat.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words for .NET
description: 探索 ParagraphFormat Borders 属性，轻松管理和自定义段落边框，增强文档的美观性和可读性。
type: docs
weight: 60
url: /zh/net/aspose.words/paragraphformat/borders/
---
## ParagraphFormat.Borders property

获取段落边框的集合。

```csharp
public BorderCollection Borders { get; }
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

* class [BorderCollection](../../bordercollection/)
* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
