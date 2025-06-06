---
title: FindReplaceOptions.FindWholeWordsOnly
linktitle: FindWholeWordsOnly
articleTitle: FindWholeWordsOnly
second_title: Aspose.Words for .NET
description: 了解 FindWholeWordsOnly 属性如何通过准确的结果增强您的搜索，确保 oldValue 仅作为独立单词匹配。
type: docs
weight: 50
url: /zh/net/aspose.words.replacing/findreplaceoptions/findwholewordsonly/
---
## FindReplaceOptions.FindWholeWordsOnly property

True 表示 oldValue 必须是一个独立的词。

```csharp
public bool FindWholeWordsOnly { get; set; }
```

## 例子

显示如何切换独立的仅限单词的查找和替换操作。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
FindReplaceOptions options = new FindReplaceOptions();

// 如果找到的文本不是另一个单词的一部分，则将“FindWholeWordsOnly”标志设置为“true”以替换找到的文本。
// 将“FindWholeWordsOnly”标志设置为“false”以替换所有文本，无论其周围环境如何。
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### 也可以看看

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)
