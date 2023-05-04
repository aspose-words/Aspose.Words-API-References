---
title: TxtLoadOptions.AutoNumberingDetection
linktitle: AutoNumberingDetection
articleTitle: AutoNumberingDetection
second_title: Aspose.Words for .NET
description: TxtLoadOptions AutoNumberingDetection property. Gets or sets a boolean value indicating either automatic numbering detection will be performed while loading a document. The default value is true in C#.
type: docs
weight: 20
url: /net/aspose.words.loading/txtloadoptions/autonumberingdetection/
---
## TxtLoadOptions.AutoNumberingDetection property

Gets or sets a boolean value indicating either automatic numbering detection will be performed while loading a document. The default value is `true`.

```csharp
public bool AutoNumberingDetection { get; set; }
```

## Examples

Shows how to disable automatic numbering detection.

```csharp
TxtLoadOptions options = new TxtLoadOptions { AutoNumberingDetection = false };
Document doc = new Document(MyDir + "Number detection.txt", options);
```

### See Also

* class [TxtLoadOptions](../)
* namespace [Aspose.Words.Loading](../../txtloadoptions/)
* assembly [Aspose.Words](../../../)
