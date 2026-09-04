---
title: AdvancedCompareOptions.CompareListDefinitions
linktitle: CompareListDefinitions
articleTitle: CompareListDefinitions
second_title: Aspose.Words for .NET
description: AdvancedCompareOptions CompareListDefinitions property. Specifies whether list definition contents are compared instead of list definition Ids.
type: docs
weight: 20
url: /net/aspose.words.comparing/advancedcompareoptions/comparelistdefinitions/
---
## AdvancedCompareOptions.CompareListDefinitions property

Specifies whether list definition contents are compared instead of list definition Ids.

```csharp
public bool CompareListDefinitions { get; set; }
```

## Remarks

Default value is `false`.

## Examples

Shows how to control whether list definition content will be compared during document comparison.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.ListFormat.ApplyNumberDefault();
builderA.Writeln("Item 1");
builderA.Writeln("Item 2");
builderA.ListFormat.RemoveNumbers();

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.ListFormat.ApplyBulletDefault();
builderB.Writeln("Item 1");
builderB.Writeln("Item 2");
builderB.ListFormat.RemoveNumbers();

// Compare documents with CompareListDefinitions enabled.
CompareOptions options = new CompareOptions()
{
    AdvancedOptions = { CompareListDefinitions = isCompareListDefinitions }
};
docA.Compare(docB, "test", DateTime.Now, options);
```

### See Also

* class [AdvancedCompareOptions](../)
* namespace [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* assembly [Aspose.Words](../../../)
