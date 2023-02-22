---
title: Font.DoubleStrikeThrough
second_title: Aspose.Words for .NET API 参考
description: Font 财产. 如果字体格式为双删除线文本则为真
type: docs
weight: 90
url: /zh/net/aspose.words/font/doublestrikethrough/
---
## Font.DoubleStrikeThrough property

如果字体格式为双删除线文本，则为真。

```csharp
public bool DoubleStrikeThrough { get; set; }
```

### 例子

演示如何在文本中添加删除线。

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
* 命名空间 [Aspose.Words](../../font/)
* 部件 [Aspose.Words](../../../)


