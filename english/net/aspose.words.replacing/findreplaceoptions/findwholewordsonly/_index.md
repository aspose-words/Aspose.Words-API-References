---
title: FindReplaceOptions.FindWholeWordsOnly
linktitle: FindWholeWordsOnly
articleTitle: FindWholeWordsOnly
second_title: Aspose.Words for .NET
description: Discover how the FindWholeWordsOnly property enhances your search with accurate results, ensuring oldValue matches only as a standalone word.
type: docs
weight: 50
url: /net/aspose.words.replacing/findreplaceoptions/findwholewordsonly/
---
## FindReplaceOptions.FindWholeWordsOnly property

True indicates the oldValue must be a standalone word.

```csharp
public bool FindWholeWordsOnly { get; set; }
```

## Examples

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

Assert.That(doc.GetText().Trim(), Is.EqualTo(findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville."));
```

### See Also

* class [FindReplaceOptions](../)
* namespace [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assembly [Aspose.Words](../../../)
