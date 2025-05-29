---
title: Font.StrikeThrough
linktitle: StrikeThrough
articleTitle: StrikeThrough
second_title: Aspose.Words for .NET
description: 探索字体删除线属性。轻松使用删除线格式化文本，让您的设计更具视觉冲击力。立即提升可读性！
type: docs
weight: 400
url: /zh/net/aspose.words/font/strikethrough/
---
## Font.StrikeThrough property

如果字体格式为删除线文本，则为真。

```csharp
public bool StrikeThrough { get; set; }
```

## 例子

展示如何为文本添加删除线。

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

Run run = new Run(doc, "Text with a single-line strikethrough.");
run.Font.StrikeThrough = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

run = new Run(doc, "Text with a double-line strikethrough.");
run.Font.DoubleStrikeThrough = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.StrikeThrough.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
