---
title: FindReplaceOptions.IgnoreFieldCodes
linktitle: IgnoreFieldCodes
articleTitle: IgnoreFieldCodes
second_title: 用于 .NET 的 Aspose.Words
description: FindReplaceOptions IgnoreFieldCodes 财产. 获取或设置一个布尔值指示忽略字段代码内的文本 默认值为错误的 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.replacing/findreplaceoptions/ignorefieldcodes/
---
## FindReplaceOptions.IgnoreFieldCodes property

获取或设置一个布尔值，指示忽略字段代码内的文本。 默认值为`错误的`.

```csharp
public bool IgnoreFieldCodes { get; set; }
```

## 评论

该选项仅影响字段代码（它不会忽略 之间的节点FieldSeparator和FieldEnd）。

要忽略整个字段，请使用相应的选项[`IgnoreFields`](../ignorefields/)。

## 例子

演示如何忽略域代码内的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("INCLUDETEXT", "Test IT!");

FindReplaceOptions options = new FindReplaceOptions {IgnoreFieldCodes = ignoreFieldCodes};

// 替换文档中的“T”，忽略字段代码内的文本。
doc.Range.Replace(new Regex("T"), "*", options);
Console.WriteLine(doc.GetText());

Assert.AreEqual(
    ignoreFieldCodes
        ? "\u0013INCLUDETEXT\u0014*est I*!\u0015"
        : "\u0013INCLUDE*EX*\u0014*est I*!\u0015", doc.GetText().Trim());
```

### 也可以看看

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)
