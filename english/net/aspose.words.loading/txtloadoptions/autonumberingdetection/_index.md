---
title: TxtLoadOptions.AutoNumberingDetection
linktitle: AutoNumberingDetection
articleTitle: AutoNumberingDetection
second_title: Aspose.Words for .NET
description: Discover TxtLoadOptions' AutoNumberingDetection property. Easily enable or disable automatic numbering for seamless document loading. Default is true.
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
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
