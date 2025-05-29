---
title: EmphasisMark Enum
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.EmphasisMark 枚举，它提供多种强调类型，可增强您的文档格式。立即提升您文本的影响力！
type: docs
weight: 1870
url: /zh/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

指定强调标记的可能类型。

```csharp
public enum EmphasisMark
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 没有强调标记。 |
| OverSolidCircle | `1` | 强调标记是显示在文本上方的实心黑色圆圈。 |
| OverComma | `2` | 强调符号是显示在文本上方的逗号字符。 |
| OverWhiteCircle | `3` | 强调标记是显示在文本上方的空白圆圈。 |
| UnderSolidCircle | `4` | 强调标记是显示在文本下方的实心黑色圆圈。 |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
