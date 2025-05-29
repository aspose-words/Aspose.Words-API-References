---
title: Font.Border
linktitle: Border
articleTitle: Border
second_title: Aspose.Words for .NET
description: 发现字体边框属性，它提供了可自定义的边框对象来增强您的字体样式和设计灵活性。
type: docs
weight: 60
url: /zh/net/aspose.words/font/border/
---
## Font.Border property

返回[`Border`](../../border/)指定字体边框的对象。

```csharp
public Border Border { get; }
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

* class [Border](../../border/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
