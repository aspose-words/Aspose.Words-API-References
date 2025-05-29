---
title: Font.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words for .NET
description: 探索“字体位置”属性，轻松调整文本对齐方式（以点为单位），精准控制排版。灵活定位，提升您的设计水平！
type: docs
weight: 310
url: /zh/net/aspose.words/font/position/
---
## Font.Position property

获取或设置文本相对于基线的位置（以点为单位）。 正数升高文本，负数降低文本。

```csharp
public double Position { get; set; }
```

## 例子

展示如何格式化文本以偏移其位置。

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// 将此文本行提升至基线以上 5 点。
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// 将此文本行降低至基线以下 10 点。
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

// 添加一串普通文本。
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// 添加作为下标出现的一段文本。
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// 添加以上标形式出现的一段文本。
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
