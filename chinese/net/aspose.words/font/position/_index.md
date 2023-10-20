---
title: Font.Position
linktitle: Position
articleTitle: Position
second_title: 用于 .NET 的 Aspose.Words
description: Font Position 财产. 获取或设置文本相对于基线的位置以磅为单位 正数提高文本负数降低文本 在 C#.
type: docs
weight: 300
url: /zh/net/aspose.words/font/position/
---
## Font.Position property

获取或设置文本相对于基线的位置（以磅为单位）。 正数提高文本，负数降低文本。

```csharp
public double Position { get; set; }
```

## 例子

显示如何格式化文本以偏移其位置。

```csharp
Document doc = new Document();
Paragraph para = (Paragraph) doc.GetChild(NodeType.Paragraph, 0, true);

// 将此行文本提高到基线以上 5 点。
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// 将此行文本降低到基线以下 10 个点。
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

// 添加一段普通文本。
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// 添加一系列显示为下标的文本。
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// 添加一系列显示为上标的文本。
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
