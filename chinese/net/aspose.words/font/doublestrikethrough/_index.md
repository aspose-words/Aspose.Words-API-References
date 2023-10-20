---
title: Font.DoubleStrikeThrough
linktitle: DoubleStrikeThrough
articleTitle: DoubleStrikeThrough
second_title: 用于 .NET 的 Aspose.Words
description: Font DoubleStrikeThrough 财产. 如果字体格式为双删除线文本则为 True 在 C#.
type: docs
weight: 90
url: /zh/net/aspose.words/font/doublestrikethrough/
---
## Font.DoubleStrikeThrough property

如果字体格式为双删除线文本，则为 True。

```csharp
public bool DoubleStrikeThrough { get; set; }
```

## 例子

演示如何向文本添加行删除线。

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
