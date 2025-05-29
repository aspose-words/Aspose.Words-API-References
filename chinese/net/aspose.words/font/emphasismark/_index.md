---
title: Font.EmphasisMark
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words for .NET
description: 了解如何使用字体强调符号属性来增强文本格式。学习如何设置和自定义强调符号，以提高可读性。
type: docs
weight: 110
url: /zh/net/aspose.words/font/emphasismark/
---
## Font.EmphasisMark property

获取或设置应用于此格式的强调符号。

```csharp
public EmphasisMark EmphasisMark { get; set; }
```

## 例子

展示如何在字形字符上方/下方添加渲染的附加字符。

```csharp
DocumentBuilder builder = new DocumentBuilder();

// 可能的强调标记类型：
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.Font.EmphasisMark = emphasisMark; 

builder.Write("Emphasis text");
builder.Writeln();
builder.Font.ClearFormatting();
builder.Write("Simple text");

builder.Document.Save(ArtifactsDir + "Fonts.SetEmphasisMark.docx");
```

### 也可以看看

* enum [EmphasisMark](../../emphasismark/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
