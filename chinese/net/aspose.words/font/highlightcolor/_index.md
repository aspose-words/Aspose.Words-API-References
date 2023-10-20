---
title: Font.HighlightColor
linktitle: HighlightColor
articleTitle: HighlightColor
second_title: 用于 .NET 的 Aspose.Words
description: Font HighlightColor 财产. 获取或设置高亮标记颜色 在 C#.
type: docs
weight: 150
url: /zh/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

获取或设置高亮（标记）颜色。

```csharp
public Color HighlightColor { get; set; }
```

## 例子

显示如何使用其字体属性格式化文本运行。

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
