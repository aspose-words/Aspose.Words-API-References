---
title: AdvancedCompareOptions Class
linktitle: AdvancedCompareOptions
articleTitle: AdvancedCompareOptions
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.AdvancedCompareOptions class for powerful document comparison. Customize settings for precise results and enhanced productivity.
type: docs
weight: 460
url: /net/aspose.words.comparing/advancedcompareoptions/
---
## AdvancedCompareOptions class

Allows to set advanced compare options.

```csharp
public class AdvancedCompareOptions
```

## Constructors

| Name | Description |
| --- | --- |
| [AdvancedCompareOptions](advancedcompareoptions/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [IgnoreDmlUniqueId](../../aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/) { get; set; } | Specifies whether to ignore difference in DrawingML unique Id. |
| [IgnoreStoreItemId](../../aspose.words.comparing/advancedcompareoptions/ignorestoreitemid/) { get; set; } | Specifies whether to ignore difference in StructuredDocumentTag store item Id. |

## Remarks

These options have no equivalence in Microsoft Word and might help to produce more precise comparison result.

## Examples

Shows how to compare SDT with same content but different store item id.

```csharp
Document docA = new Document(MyDir + "Document with SDT 1.docx");
Document docB = new Document(MyDir + "Document with SDT 2.docx");

// Configure options to compare SDT with same content but different store item id.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreStoreItemId = false;

docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.That(docA.Revisions.Count, Is.EqualTo(8));

compareOptions.AdvancedOptions.IgnoreStoreItemId = true;

docA.Revisions.RejectAll();
docA.Compare(docB, "user", DateTime.Now, compareOptions);
Assert.That(docA.Revisions.Count, Is.EqualTo(0));
```

### See Also

* namespace [Aspose.Words.Comparing](../../aspose.words.comparing/)
* assembly [Aspose.Words](../../)
