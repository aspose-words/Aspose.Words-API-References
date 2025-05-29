---
title: Border.LineStyle
linktitle: LineStyle
articleTitle: LineStyle
second_title: Aspose.Words for .NET
description: 使用 Border LineStyle 属性自定义您的设计，让您轻松获取或设置独特的边框样式以增强视觉吸引力。
type: docs
weight: 40
url: /zh/net/aspose.words/border/linestyle/
---
## Border.LineStyle property

获取或设置边框样式。

```csharp
public LineStyle LineStyle { get; set; }
```

## 评论

如果将线条样式设置为无，则线条宽度将自动更改为零。

## 例子

展示如何将带边框的字符串插入文档。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

### 也可以看看

* enum [LineStyle](../../linestyle/)
* class [Border](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
