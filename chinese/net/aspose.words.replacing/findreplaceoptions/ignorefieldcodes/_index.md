---
title: FindReplaceOptions.IgnoreFieldCodes
linktitle: IgnoreFieldCodes
articleTitle: IgnoreFieldCodes
second_title: Aspose.Words for .NET
description: 探索 FindReplaceOptions 的 IgnoreFieldCodes 属性，轻松管理字段代码中的文本。只需简单的布尔值设置即可控制可见性！
type: docs
weight: 70
url: /zh/net/aspose.words.replacing/findreplaceoptions/ignorefieldcodes/
---
## FindReplaceOptions.IgnoreFieldCodes property

获取或设置一个布尔值，指示是否忽略字段代码内的文本。 默认值为`错误的`.

```csharp
public bool IgnoreFieldCodes { get; set; }
```

## 评论

此选项仅影响字段代码（它不会忽略 之间的节点）FieldSeparator和FieldEnd）。

要忽略整个字段，请使用相应的选项[`IgnoreFields`](../ignorefields/)。

## 例子

显示如何忽略字段代码内的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField("INCLUDETEXT", "Test IT!");

FindReplaceOptions options = new FindReplaceOptions {IgnoreFieldCodes = ignoreFieldCodes};

// 是否忽略字段代码内的文本，替换文档中的“T”。
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
