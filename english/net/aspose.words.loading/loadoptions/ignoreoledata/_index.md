---
title: LoadOptions.IgnoreOleData
linktitle: IgnoreOleData
second_title: Aspose.Words for .NET API Reference
description: LoadOptions IgnoreOleData property. Specifies whether to ignore the OLE data in C#.
type: docs
weight: 70
url: /net/aspose.words.loading/loadoptions/ignoreoledata/
---
## IgnoreOleData property

Specifies whether to ignore the OLE data.

```csharp
public bool IgnoreOleData { get; set; }
```

## Remarks

Ignoring OLE data may reduce memory consumption and increase performance without data lost in a case when destination format does not support OLE objects.

The default value is `false`.

## Examples

Shows how to ingore OLE data while loading.

```csharp
// Ignoring OLE data may reduce memory consumption and increase performance
// without data lost in a case when destination format does not support OLE objects.
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Document doc = new Document(MyDir + "OLE objects.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.IgnoreOleData.docx");
```

### See Also

* class [LoadOptions](../)
* namespace [Aspose.Words.Loading](../../loadoptions/)
* assembly [Aspose.Words](../../../)
