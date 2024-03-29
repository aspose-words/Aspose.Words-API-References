---
title: Font.Border
linktitle: Border
articleTitle: Border
second_title: 用于 .NET 的 Aspose.Words
description: Font Border 财产. 返回一个Border指定字体边框的对象 在 C#.
type: docs
weight: 60
url: /zh/net/aspose.words/font/border/
---
## Font.Border property

返回一个[`Border`](../../border/)指定字体边框的对象。

```csharp
public Border Border { get; }
```

## 例子

演示如何将边框包围的字符串插入到文档中。

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

* class [Border](../../border/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
