---
title: FindReplaceOptions.IgnoreInserted
linktitle: IgnoreInserted
articleTitle: IgnoreInserted
second_title: 用于 .NET 的 Aspose.Words
description: FindReplaceOptions IgnoreInserted 财产. 获取或设置一个布尔值指示忽略插入修订中的文本 默认值为错误的 在 C#.
type: docs
weight: 100
url: /zh/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

获取或设置一个布尔值，指示忽略插入修订中的文本。 默认值为`错误的`.

```csharp
public bool IgnoreInserted { get; set; }
```

## 例子

演示如何在查找和替换操作期间包含或忽略插入修订内的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// 开始跟踪修订并插入一个段落。该段落将是插入修订。
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
FindReplaceOptions options = new FindReplaceOptions();

// 将“IgnoreInserted”标志设置为“true”以获取查找和替换
// 忽略插入修订的段落的操作。
// 将“IgnoreInserted”标志设置为“false”以获取查找和替换
// 还可以在插入修订中搜索文本的操作。
options.IgnoreInserted = ignoreTextInsideInsertRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideInsertRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### 也可以看看

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)
