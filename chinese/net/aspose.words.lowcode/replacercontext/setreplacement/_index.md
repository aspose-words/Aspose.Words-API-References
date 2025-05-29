---
title: ReplacerContext.SetReplacement
linktitle: SetReplacement
articleTitle: SetReplacement
second_title: Aspose.Words for .NET
description: 使用 ReplacerContext SetReplacement 方法增强您的查找和替换操作，从而实现无缝的模式和替换管理以提高效率。
type: docs
weight: 30
url: /zh/net/aspose.words.lowcode/replacercontext/setreplacement/
---
## SetReplacement(*string, string*) {#setreplacement}

设置查找/替换操作使用的模式和替换。

```csharp
public void SetReplacement(string pattern, string replacement)
```

## 评论

使用此方法会覆盖先前设置的模式和替换。

## 例子

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

### 也可以看看

* class [ReplacerContext](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)

---

## SetReplacement(*Regex, string*) {#setreplacement_1}

设置查找/替换操作使用的模式和替换。

```csharp
public void SetReplacement(Regex pattern, string replacement)
```

## 评论

使用此方法会覆盖先前设置的模式和替换。

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

* class [ReplacerContext](../)
* 命名空间 [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* 部件 [Aspose.Words](../../../)
