---
title: FindReplaceOptions.MatchCase
linktitle: MatchCase
articleTitle: MatchCase
second_title: Aspose.Words for .NET
description: 探索 FindReplaceOptions 中的 MatchCase 属性，启用区分大小写或不区分大小写的比较，实现精准的文本编辑。优化您的工作流程！
type: docs
weight: 140
url: /zh/net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

True 表示区分大小写比较，false 表示不区分大小写比较。

```csharp
public bool MatchCase { get; set; }
```

## 例子

展示如何在执行查找和替换操作时切换区分大小写。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
FindReplaceOptions options = new FindReplaceOptions();

// 将“MatchCase”标志设置为“true”，以在查找要替换的字符串时应用区分大小写。
// 将“MatchCase”标志设置为“false”以在搜索要替换的文本时忽略字符大小写。
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

### 也可以看看

* class [FindReplaceOptions](../)
* 命名空间 [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../../)
