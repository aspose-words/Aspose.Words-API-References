---
title: AdvancedCompareOptions.IgnoreDmlUniqueId
linktitle: IgnoreDmlUniqueId
articleTitle: IgnoreDmlUniqueId
second_title: Aspose.Words for .NET
description: Discover the AdvancedCompareOptions IgnoreDmlUniqueId property to enhance your DrawingML processing by efficiently managing unique IDs. Optimize your workflow!
type: docs
weight: 20
url: /net/aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/
---
## AdvancedCompareOptions.IgnoreDmlUniqueId property

Specifies whether to ignore difference in DrawingML unique Id.

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

## Remarks

Default value is `false`.

## Examples

Shows how to compare documents ignoring DML unique ID.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// By default, Aspose.Words do not ignore DML's unique ID, and the revisions count was 2.
// If we are ignoring DML's unique ID, and revisions count were 0.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.That(docA.Revisions.Count, Is.EqualTo(isIgnoreDmlUniqueId ? 0 : 2));
```

### See Also

* class [AdvancedCompareOptions](../)
* namespace [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* assembly [Aspose.Words](../../../)
