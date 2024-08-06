---
title: CompareOptions.AdvancedOptions
linktitle: AdvancedOptions
articleTitle: AdvancedOptions
second_title: Aspose.Words for .NET
description: CompareOptions AdvancedOptions property. Specifies advanced compare options that might help to produce more precise comparison output in C#.
type: docs
weight: 20
url: /net/aspose.words.comparing/compareoptions/advancedoptions/
---
## CompareOptions.AdvancedOptions property

Specifies advanced compare options that might help to produce more precise comparison output.

```csharp
public AdvancedCompareOptions AdvancedOptions { get; }
```

## Examples

Shows how to compare documents ignoring DML unique ID.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// By default, Aspose.Words do not ignore DML's unique ID, and the revisions count was 2.
// If we are ignoring DML's unique ID, and revisions count were 0.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.AdvancedOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### See Also

* class [AdvancedCompareOptions](../../advancedcompareoptions/)
* class [CompareOptions](../)
* namespace [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* assembly [Aspose.Words](../../../)
