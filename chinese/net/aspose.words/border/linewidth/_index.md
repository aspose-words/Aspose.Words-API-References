---
title: Border.LineWidth
linktitle: LineWidth
articleTitle: LineWidth
second_title: Aspose.Words for .NET
description: 调整边框线宽属性以点为单位自定义边框粗细，增强设计的精确度和视觉吸引力。
type: docs
weight: 50
url: /zh/net/aspose.words/border/linewidth/
---
## Border.LineWidth property

获取或设置边框宽度（以点为单位）。

```csharp
public double LineWidth { get; set; }
```

## 评论

如果在线样式为无时设置线宽大于零，则线样式 is 会自动更改为单线。

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

* class [Border](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
