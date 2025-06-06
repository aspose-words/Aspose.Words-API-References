---
title: FindReplaceOptions.IgnoreDeleted
linktitle: IgnoreDeleted
articleTitle: IgnoreDeleted
second_title: Aspose.Words for .NET
description: 探索 FindReplaceOptions 的 IgnoreDeleted 属性，通过简单的布尔值切换控制已删除修订中的文本可见性。提升您的编辑体验！
type: docs
weight: 60
url: /zh/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

获取或设置一个布尔值，指示是否忽略删除修订版中的文本。 默认值为`错误的`.

```csharp
public bool IgnoreDeleted { get; set; }
```

## 例子

展示如何在查找和替换操作期间包含或忽略删除修订中的文本。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// 开始跟踪修订并删除第二段，这将创建删除修订。
// 该段落将保留在文档中，直到我们接受删除修订。
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
FindReplaceOptions options = new FindReplaceOptions();

// 将“IgnoreDeleted”标志设置为“true”以获取查找和替换
// 忽略删除修订的段落的操作。
// 将“IgnoreDeleted”标志设置为“false”以获取查找和替换
// 操作还会搜索删除修订版中的文本。
options.IgnoreDeleted = ignoreTextInsideDeleteRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideDeleteRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### 也可以看看

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)
