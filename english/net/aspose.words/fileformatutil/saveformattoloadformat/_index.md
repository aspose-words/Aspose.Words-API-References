---
title: FileFormatUtil.SaveFormatToLoadFormat
linktitle: SaveFormatToLoadFormat
articleTitle: SaveFormatToLoadFormat
second_title: Aspose.Words for .NET
description: Effortlessly convert SaveFormat to LoadFormat with the FileFormatUtil method. Simplify file management and enhance compatibility today!
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
