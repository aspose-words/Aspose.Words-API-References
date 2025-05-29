---
title: ReplacerContext Class
linktitle: ReplacerContext
articleTitle: ReplacerContext
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words LowCode ReplacerContext 类，实现无缝查找和替换操作，增强文档自动化和效率。
type: docs
weight: 4350
url: /zh/net/aspose.words.lowcode/replacercontext/
---
## ReplacerContext class

查找/替换操作上下文。

```csharp
public class ReplacerContext : ProcessorContext
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [ReplacerContext](replacercontext/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [FindReplaceOptions](../../aspose.words.lowcode/replacercontext/findreplaceoptions/) { get; } | 查找/替换选项。 |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | 处理器使用的字体设置。 |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | 处理器使用的文档布局选项。 |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | 处理器使用的警告回调。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement_1)(*Regex, string*) | 设置查找/替换操作使用的模式和替换。 |
| [SetReplacement](../../aspose.words.lowcode/replacercontext/setreplacement/#setreplacement)(*string, string*) | 设置查找/替换操作使用的模式和替换。 |

## 例子

展示如何使用上下文在文档中用正则表达式替换字符串。

```csharp
// 有几种方法可以在文档中使用正则表达式替换字符串：
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

ReplacerContext replacerContext = new ReplacerContext();
replacerContext.SetReplacement(pattern, replacement);
replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

Replacer.Create(replacerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.ReplaceContextRegex.docx")
    .Execute();
```

展示如何使用上下文替换文档中的字符串。

```csharp
// 有几种方法可以替换文档中的字符串：
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

ReplacerContext replacerContext = new ReplacerContext();
replacerContext.SetReplacement(pattern, replacement);
replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

Replacer.Create(replacerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.ReplaceContext.docx")
    .Execute();
```

展示如何使用上下文中的流中的文档替换文档中的字符串。

```csharp
// 有几种方法可以使用流中的文档替换文档中的字符串：
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    ReplacerContext replacerContext = new ReplacerContext();
    replacerContext.SetReplacement(pattern, replacement);
    replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Create(replacerContext)
        .From(streamIn)
        .To(streamOut, SaveFormat.Docx)
        .Execute();
}
```

展示如何使用来自上下文的流中的文档在文档中用正则表达式替换字符串。

```csharp
// 有几种方法可以使用流中的文档将文档中的字符串替换为正则表达式：
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    ReplacerContext replacerContext = new ReplacerContext();
    replacerContext.SetReplacement(pattern, replacement);
    replacerContext.FindReplaceOptions.FindWholeWordsOnly = false;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ReplaceContextStreamRegex.docx", FileMode.Create, FileAccess.ReadWrite))
        Replacer.Create(replacerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### 也可以看看

* class [ProcessorContext](../processorcontext/)
* 命名空间 [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../)
