---
title: FindReplaceOptions.FindWholeWordsOnly
linktitle: FindWholeWordsOnly
articleTitle: FindWholeWordsOnly
second_title: Aspose.Words for .NET
description: FindReplaceOptions FindWholeWordsOnly property. True indicates the oldValue must be a standalone word in C#.
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

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### See Also

* class [FindReplaceOptions](../)
* namespace [Aspose.Words.Replacing](../../findreplaceoptions/)
* assembly [Aspose.Words](../../../)
