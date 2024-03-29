---
title: FileFormatUtil.SaveFormatToLoadFormat
linktitle: SaveFormatToLoadFormat
articleTitle: SaveFormatToLoadFormat
second_title: Aspose.Words for .NET
description: FileFormatUtil SaveFormatToLoadFormat method. Converts a SaveFormat value to a LoadFormat value if possible in C#.
type: docs
weight: 90
url: /net/aspose.words/fileformatutil/saveformattoloadformat/
---
## FileFormatUtil.SaveFormatToLoadFormat method

Converts a [`SaveFormat`](../../saveformat/) value to a [`LoadFormat`](../../loadformat/) value if possible.

```csharp
public static LoadFormat SaveFormatToLoadFormat(SaveFormat saveFormat)
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentException | Throws when cannot convert. |

## Examples

Shows how to convert a save format to its corresponding load format.

```csharp
Assert.AreEqual(LoadFormat.Html, FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Html));

// Some file types can have documents saved to, but not loaded from using Aspose.Words.
// If we attempt to convert a save format of such a type to a load format, an exception will be thrown.
Assert.Throws<ArgumentException>(() => FileFormatUtil.SaveFormatToLoadFormat(SaveFormat.Jpeg));
```

### See Also

* enum [LoadFormat](../../loadformat/)
* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
