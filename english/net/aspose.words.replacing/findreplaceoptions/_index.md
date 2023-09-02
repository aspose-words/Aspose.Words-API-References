---
title: FindReplaceOptions Class
linktitle: FindReplaceOptions
articleTitle: FindReplaceOptions
second_title: Aspose.Words for .NET
description: Aspose.Words.Replacing.FindReplaceOptions class. Specifies options for find/replace operations in C#.
type: docs
weight: 4620
url: /net/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class

Specifies options for find/replace operations.

To learn more, visit the [Find and Replace](https://docs.aspose.com/words/net/find-and-replace/) documentation article.

```csharp
public class FindReplaceOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [FindReplaceOptions](findreplaceoptions/#constructor)() | The default constructor. |
| [FindReplaceOptions](findreplaceoptions/#constructor_1)(*[FindReplaceDirection](../findreplacedirection/)*) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_3)(*[IReplacingCallback](../ireplacingcallback/)*) |  |
| [FindReplaceOptions](findreplaceoptions/#constructor_2)(*[FindReplaceDirection](../findreplacedirection/), [IReplacingCallback](../ireplacingcallback/)*) |  |

## Properties

| Name | Description |
| --- | --- |
| [ApplyFont](../../aspose.words.replacing/findreplaceoptions/applyfont/) { get; } | Text formatting applied to new content. |
| [ApplyParagraphFormat](../../aspose.words.replacing/findreplaceoptions/applyparagraphformat/) { get; } | Paragraph formatting applied to new content. |
| [Direction](../../aspose.words.replacing/findreplaceoptions/direction/) { get; set; } | Selects direction for replace. Default value is Forward. |
| [FindWholeWordsOnly](../../aspose.words.replacing/findreplaceoptions/findwholewordsonly/) { get; set; } | True indicates the oldValue must be a standalone word. |
| [IgnoreDeleted](../../aspose.words.replacing/findreplaceoptions/ignoredeleted/) { get; set; } | Gets or sets a boolean value indicating either to ignore text inside delete revisions. The default value is `false`. |
| [IgnoreFieldCodes](../../aspose.words.replacing/findreplaceoptions/ignorefieldcodes/) { get; set; } | Gets or sets a boolean value indicating either to ignore text inside field codes. The default value is `false`. |
| [IgnoreFields](../../aspose.words.replacing/findreplaceoptions/ignorefields/) { get; set; } | Gets or sets a boolean value indicating either to ignore text inside fields. The default value is `false`. |
| [IgnoreFootnotes](../../aspose.words.replacing/findreplaceoptions/ignorefootnotes/) { get; set; } | Gets or sets a boolean value indicating either to ignore footnotes. The default value is `false`. |
| [IgnoreInserted](../../aspose.words.replacing/findreplaceoptions/ignoreinserted/) { get; set; } | Gets or sets a boolean value indicating either to ignore text inside insert revisions. The default value is `false`. |
| [IgnoreShapes](../../aspose.words.replacing/findreplaceoptions/ignoreshapes/) { get; set; } | Gets or sets a boolean value indicating either to ignore shapes within a text. |
| [IgnoreStructuredDocumentTags](../../aspose.words.replacing/findreplaceoptions/ignorestructureddocumenttags/) { get; set; } | Gets or sets a boolean value indicating either to ignore content of [`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/). The default value is `false`. |
| [LegacyMode](../../aspose.words.replacing/findreplaceoptions/legacymode/) { get; set; } | Gets or sets a boolean value indicating that old find/replace algorithm is used. |
| [MatchCase](../../aspose.words.replacing/findreplaceoptions/matchcase/) { get; set; } | True indicates case-sensitive comparison, false indicates case-insensitive comparison. |
| [ReplacingCallback](../../aspose.words.replacing/findreplaceoptions/replacingcallback/) { get; set; } | The user-defined method which is called before every replace occurrence. |
| [SmartParagraphBreakReplacement](../../aspose.words.replacing/findreplaceoptions/smartparagraphbreakreplacement/) { get; set; } | Gets or sets a boolean value indicating either it is allowed to replace paragraph break when there is no next sibling paragraph. |
| [UseLegacyOrder](../../aspose.words.replacing/findreplaceoptions/uselegacyorder/) { get; set; } | True indicates that a text search is performed sequentially from top to bottom considering the text boxes. Default value is `false`. |
| [UseSubstitutions](../../aspose.words.replacing/findreplaceoptions/usesubstitutions/) { get; set; } | Gets or sets a boolean value indicating whether to recognize and use substitutions within replacement patterns. The default value is `false`. |

## Examples

Shows how to toggle case sensitivity when performing a find-and-replace operation.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Ruby bought a ruby necklace.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
FindReplaceOptions options = new FindReplaceOptions();

// Set the "MatchCase" flag to "true" to apply case sensitivity while finding strings to replace.
// Set the "MatchCase" flag to "false" to ignore character case while searching for text to replace.
options.MatchCase = matchCase;

doc.Range.Replace("Ruby", "Jade", options);

Assert.AreEqual(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace.",
    doc.GetText().Trim());
```

Shows how to toggle standalone word-only find-and-replace operations.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
FindReplaceOptions options = new FindReplaceOptions();

// Set the "FindWholeWordsOnly" flag to "true" to replace the found text if it is not a part of another word.
// Set the "FindWholeWordsOnly" flag to "false" to replace all text regardless of its surroundings.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### See Also

* namespace [Aspose.Words.Replacing](../../aspose.words.replacing/)
* assembly [Aspose.Words](../../)
