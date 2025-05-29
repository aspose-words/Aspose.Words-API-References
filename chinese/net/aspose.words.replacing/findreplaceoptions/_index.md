---
title: FindReplaceOptions Class
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.FindReplaceOptions 类的高级查找和替换功能，增强文档编辑的精确性和灵活性。
type: docs
weight: 5350
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
| [FindReplaceOptions](findreplaceoptions/#constructor)() | 使用默认设置初始化 FindReplaceOptions 类的新实例。 |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(*[FindReplaceDirection](../findreplacedirection/)*) | 使用指定的方向初始化 FindReplaceOptions 类的新实例。 |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(*[IReplacingCallback](../ireplacingcallback/)*) | 使用指定的替换回调初始化 FindReplaceOptions 类的新实例。 |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(*[FindReplaceDirection](../findreplacedirection/), [IReplacingCallback](../ireplacingcallback/)*) | 使用指定的方向和替换回调初始化 FindReplaceOptions 类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | 文本格式已应用于新内容。 |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | 段落格式已应用于新内容。 |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | 选择替换方向。默认值为Forward. |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | True 表示 oldValue 必须是一个独立的词。 |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | 获取或设置一个布尔值，指示是否忽略删除修订版中的文本。 默认值为`错误的`. |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | 获取或设置一个布尔值，指示是否忽略字段代码内的文本。 默认值为`错误的`. |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | 获取或设置一个布尔值，指示是否忽略字段内的文本。 默认值为`错误的`. |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | 获取或设置一个布尔值，指示是否忽略脚注。 默认值为`错误的`. |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | 获取或设置一个布尔值，指示是否忽略插入修订中的文本。 默认值为`错误的`. |
| [IgnoreShapes](../../aspose.words.replacing/findreplaceoptions/ignoreshapes/) { get; set; } | 获取或设置一个布尔值，指示是否忽略文本中的形状。 |
| [IgnoreStructuredDocumentTags](../../aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/) { get; set; } | 获取或设置一个布尔值，指示忽略的内容[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/). 默认值为`错误的`. |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | 获取或设置一个布尔值，指示使用旧的查找/替换算法。 |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | True 表示区分大小写比较，false 表示不区分大小写比较。 |
| [ReplacementFormat](../../aspose.words.replacing/findreplaceoptions/replacementformat/) { get; set; } | 指定替换的格式。默认为Text. |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | 每次替换发生之前调用的用户定义方法。 |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | 获取或设置一个布尔值，指示当没有下一个同级段落时是否允许替换段落 break 。 |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True 表示考虑文本框，按从上到下的顺序执行文本搜索。 默认值为`错误的`. |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | 获取或设置一个布尔值，指示是否识别并使用替换模式中的替换。 默认值为`错误的`. |

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

* 命名空间 [Aspose.Words.Replacing](../../aspose.words.replacing/)
* 部件 [Aspose.Words](../../)
