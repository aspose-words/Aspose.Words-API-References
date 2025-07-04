---
title: WarningInfoCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: Discover the WarningInfoCollection Count property to easily access the total number of elements in your collection for efficient data management.
type: docs
weight: 20
url: /net/aspose.words/warninginfocollection/count/
---
## WarningInfoCollection.Count property

Gets the number of elements contained in the collection.

```csharp
public int Count { get; }
```

## Examples

Shows how to get warnings about unsupported formats.

```csharp
WarningInfoCollection warnings = new WarningInfoCollection();
Document doc = new Document(MyDir + "FB2 document.fb2", new LoadOptions { WarningCallback = warnings });

Assert.That(warnings[0].Description, Is.EqualTo("The original file load format is FB2, which is not supported by Aspose.Words. The file is loaded as an XML document."));
Assert.That(warnings.Count, Is.EqualTo(1));
```

### See Also

* class [WarningInfoCollection](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
