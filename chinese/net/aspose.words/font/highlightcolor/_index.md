---
title: Font.HighlightColor
linktitle: HighlightColor
articleTitle: HighlightColor
second_title: Aspose.Words for .NET
description: 探索字体高亮颜色属性——轻松自定义文本高亮颜色，提升可读性和视觉吸引力。提升您的设计！
type: docs
weight: 150
url: /zh/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

获取或设置突出显示（标记）颜色。

```csharp
public Color HighlightColor { get; set; }
```

## 例子

展示如何使用字体属性来格式化文本。

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
