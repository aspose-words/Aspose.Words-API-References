---
title: EmphasisMark
second_title: Aspose.Words for .NET API 参考
description: 指定可能的强调标记类型
type: docs
weight: 1310
url: /zh/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

指定可能的强调标记类型。

```csharp
public enum EmphasisMark
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 没有强调标记。 |
| OverSolidCircle | `1` | 强调标记是显示在文本上方的实心黑色圆圈。 |
| OverComma | `2` | 强调标记是显示在文本上方的逗号字符。 |
| OverWhiteCircle | `3` | 强调标记是显示在文本上方的一个空白圆圈。 |
| UnderSolidCircle | `4` | 强调标记是显示在文本下方的实心黑色圆圈。 |

### 例子

显示如何添加在字形字符上方/下方呈现的附加字符。

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

* 命名空间 [Aspose.Words](../../aspose.words)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
