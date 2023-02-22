---
title: Font.EmphasisMark
second_title: Aspose.Words for .NET API 参考
description: Font 财产. 获取或设置应用于此格式的强调标记
type: docs
weight: 110
url: /zh/net/aspose.words/font/emphasismark/
---
## Font.EmphasisMark property

获取或设置应用于此格式的强调标记。

```csharp
public EmphasisMark EmphasisMark { get; set; }
```

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

* enum [EmphasisMark](../../emphasismark/)
* class [Font](../)
* 命名空间 [Aspose.Words](../../font/)
* 部件 [Aspose.Words](../../../)


