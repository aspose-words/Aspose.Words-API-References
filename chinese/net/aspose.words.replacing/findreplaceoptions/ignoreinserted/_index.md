---
title: FindReplaceOptions.IgnoreInserted
linktitle: IgnoreInserted
articleTitle: IgnoreInserted
second_title: Aspose.Words for .NET
description: 探索 FindReplaceOptions 的 IgnoreInserted 属性，通过这个简单的布尔值设置来控制插入修订中的文本处理。默认值为 false。
type: docs
weight: 100
url: /zh/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

获取或设置一个布尔值，指示是否忽略插入修订中的文本。 默认值为`错误的`.

```csharp
public bool IgnoreInserted { get; set; }
```

## 例子

展示如何在查找和替换操作期间包含或忽略插入修订中的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// 开始跟踪修订并插入一个段落。该段落将作为插入修订。
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
FindReplaceOptions options = new FindReplaceOptions();

// 将“IgnoreInserted”标志设置为“true”以获取查找和替换
// 操作忽略插入修订的段落。
// 将“IgnoreInserted”标志设置为“false”以获取查找和替换
// 操作还搜索插入修订版内的文本。
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
