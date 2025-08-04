---
title: FindReplaceOptions.MatchCase
linktitle: MatchCase
articleTitle: MatchCase
second_title: Aspose.Words for .NET
description: Discover the MatchCase property in FindReplaceOptions, enable case-sensitive or case-insensitive comparisons for precise text editing. Optimize your workflow!
type: docs
weight: 150
url: /net/aspose.words.replacing/findreplaceoptions/matchcase/
---
## FindReplaceOptions.MatchCase property

True indicates case-sensitive comparison, false indicates case-insensitive comparison.

```csharp
public bool MatchCase { get; set; }
```

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

Assert.That(doc.GetText().Trim(), Is.EqualTo(matchCase ? "Jade bought a ruby necklace." : "Jade bought a Jade necklace."));
```

### See Also

* class [FindReplaceOptions](../)
* namespace [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* assembly [Aspose.Words](../../../)
