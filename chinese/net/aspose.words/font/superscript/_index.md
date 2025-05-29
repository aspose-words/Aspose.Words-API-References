---
title: Font.Superscript
linktitle: Superscript
articleTitle: Superscript
second_title: Aspose.Words for .NET
description: 探索“字体上标”属性，轻松将文本格式化为上标，提升文档的可读性和风格。立即提升您的设计！
type: docs
weight: 450
url: /zh/net/aspose.words/font/superscript/
---
## Font.Superscript property

如果字体格式为上标，则为真。

```csharp
public bool Superscript { get; set; }
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
