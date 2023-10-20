---
title: Font.SmallCaps
linktitle: SmallCaps
articleTitle: SmallCaps
second_title: 用于 .NET 的 Aspose.Words
description: Font SmallCaps 财产. 如果字体格式为小写大写字母则为 True 在 C#.
type: docs
weight: 360
url: /zh/net/aspose.words/font/smallcaps/
---
## Font.SmallCaps property

如果字体格式为小写大写字母，则为 True。

```csharp
public bool SmallCaps { get; set; }
```

## 例子

演示如何设置运行格式以大写显示其内容。

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// 有两种方法可以让运行以大写形式显示其小写文本而不更改内容。
// 1 - 设置 AllCaps 标志以常规大写形式显示所有字符：
Run run = new Run(doc, "all capitals");
run.Font.AllCaps = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

// 2 - 设置 SmallCaps 标志以小写大写显示所有字符：
// 如果字符是小写，它将以其大写形式出现
// 但与小写字母具有相同的高度（字体的 x 高度）。
// 原来大写的字符看起来是一样的。
run = new Run(doc, "Small Capitals");
run.Font.SmallCaps = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.Caps.docx");
```

### 也可以看看

* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
