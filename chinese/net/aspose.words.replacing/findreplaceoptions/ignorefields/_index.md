---
title: FindReplaceOptions.IgnoreFields
linktitle: IgnoreFields
articleTitle: IgnoreFields
second_title: 用于 .NET 的 Aspose.Words
description: FindReplaceOptions IgnoreFields 财产. 获取或设置一个布尔值指示忽略字段内的文本 默认值为错误的 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words.replacing/findreplaceoptions/ignorefields/
---
## FindReplaceOptions.IgnoreFields property

获取或设置一个布尔值，指示忽略字段内的文本。 默认值为`错误的`.

```csharp
public bool IgnoreFields { get; set; }
```

## 评论

此选项影响整个字段（ 之间的所有节点）FieldStart和FieldEnd）。

要仅忽略字段代码，请使用相应的选项[`IgnoreFieldCodes`](../ignorefieldcodes/)。

## 例子

演示如何忽略字段内的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.InsertField("QUOTE", "Hello again!");

// 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
FindReplaceOptions options = new FindReplaceOptions();

// 将“IgnoreFields”标志设置为“true”以获取查找和替换
// 忽略字段内文本的操作。
// 将“IgnoreFields”标志设置为“false”以获取查找和替换
// 还可以搜索字段内文本的操作。
options.IgnoreFields = ignoreTextInsideFields;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideFields
        ? "Greetings world!\r\u0013QUOTE\u0014Hello again!\u0015"
        : "Greetings world!\r\u0013QUOTE\u0014Greetings again!\u0015", doc.GetText().Trim());
```

### 也可以看看

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)
