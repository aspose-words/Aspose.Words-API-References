---
title: LoadOptions.IgnoreOleData
second_title: Aspose.Words för .NET API Referens
description: LoadOptions fast egendom. Anger om OLEdata ska ignoreras.
type: docs
weight: 70
url: /sv/net/aspose.words.loading/loadoptions/ignoreoledata/
---
## LoadOptions.IgnoreOleData property

Anger om OLE-data ska ignoreras.

```csharp
public bool IgnoreOleData { get; set; }
```

### Anmärkningar

Att ignorera OLE-data kan minska minnesförbrukningen och öka prestandan utan att data går förlorade i ett fall där destinationsformatet inte stöder OLE-objekt.

Standardvärdet är`falsk`.

### Exempel

Visar hur man lägger in OLE-data under laddning.

```csharp
// Att ignorera OLE-data kan minska minnesförbrukningen och öka prestandan
// utan data förlorade i ett fall där destinationsformatet inte stöder OLE-objekt.
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Document doc = new Document(MyDir + "OLE objects.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.IgnoreOleData.docx");
```

### Se även

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../loadoptions/)
* hopsättning [Aspose.Words](../../../)


