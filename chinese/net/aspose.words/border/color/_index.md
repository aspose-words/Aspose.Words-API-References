---
title: Border.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words for .NET
description: 使用边框颜色属性轻松自定义您的设计，让您可以设置和修改边框颜色以获得惊人的视觉效果。
type: docs
weight: 10
url: /zh/net/aspose.words/border/color/
---
## Border.Color property

获取或设置边框颜色。

```csharp
public Color Color { get; set; }
```

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
