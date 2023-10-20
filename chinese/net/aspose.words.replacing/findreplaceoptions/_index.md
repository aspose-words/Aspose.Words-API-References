---
title: FindReplaceOptions Class
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Replacing.FindReplaceOptions 班级. 指定查找/替换操作的选项 在 C#.
type: docs
weight: 4620
url: /zh/net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

指定查找/替换操作的选项。

要了解更多信息，请访问[查找和替换](https://docs.aspose.com/words/net/find-and-replace/)文档文章。

```csharp
public class FindReplaceOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | 默认构造函数。 |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(*[FindReplaceDirection](../findreplacedirection/)*) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(*[IReplacingCallback](../ireplacingcallback/)*) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(*[FindReplaceDirection](../findreplacedirection/), [IReplacingCallback](../ireplacingcallback/)*) |  |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | 应用于新内容的文本格式。 |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | 段落格式应用于新内容。 |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | 选择替换方向。默认值为Forward. |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | True 表示 oldValue 必须是独立的单词。 |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | 获取或设置一个布尔值，指示忽略删除修订内的文本。 默认值为`错误的`. |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | 获取或设置一个布尔值，指示忽略字段代码内的文本。 默认值为`错误的`. |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | 获取或设置一个布尔值，指示忽略字段内的文本。 默认值为`错误的`. |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | 获取或设置一个布尔值，指示是否忽略脚注。 默认值为`错误的`. |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | 获取或设置一个布尔值，指示忽略插入修订中的文本。 默认值为`错误的`. |
| [IgnoreShapes](../../aspose.words.replacing/findreplaceoptions/ignoreshapes/) { get; set; } | 获取或设置一个布尔值，指示忽略文本中的形状。 |
| [IgnoreStructuredDocumentTags](../../aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/) { get; set; } | 获取或设置一个布尔值，指示忽略以下内容[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/). 默认值为`错误的`. |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | 获取或设置一个布尔值，指示使用旧的查找/替换算法。 |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | True 表示区分大小写比较， false 表示不区分大小写比较。 |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | 在每次替换发生之前调用的用户定义方法。 |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | 获取或设置一个布尔值，指示当没有下一个兄弟段落时是否允许替换段落break 。 |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True 表示考虑文本框从上到下顺序执行文本搜索。 默认值为`错误的`. |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | 获取或设置一个布尔值，指示是否在替换模式中识别和使用替换。 默认值为`错误的`. |

## 例子

演示如何在执行查找和替换操作时切换区分大小写。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
FindReplaceOptions options = new FindReplaceOptions();

// 将“MatchCase”标志设置为“true”以在查找要替换的字符串时应用区分大小写。
// 将“MatchCase”标志设置为“false”以在搜索要替换的文本时忽略字符大小写。
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

演示如何切换独立的仅单词查找和替换操作。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// 我们可以使用“FindReplaceOptions”对象来修改查找和替换过程。
FindReplaceOptions options = new FindReplaceOptions();

// 将“FindWholeWordsOnly”标志设置为“true”，以替换找到的文本（如果它不是另一个单词的一部分）。
// 将“FindWholeWordsOnly”标志设置为“false”以替换所有文本，无论其周围环境如何。
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### 也可以看看

* 命名空间 [Aspose.Words.Replacing](../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../)
