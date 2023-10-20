---
title: ParagraphFormat.Borders
linktitle: Borders
articleTitle: Borders
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphFormat Borders 财产. 获取段落边框的集合 在 C#.
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

演示如何插入带有上边框的段落。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders[BorderType.Top];
topBorder.Color = Color.Red;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;

builder.Writeln("Text with a red top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### 也可以看看

* class [BorderCollection](../../bordercollection/)
* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
