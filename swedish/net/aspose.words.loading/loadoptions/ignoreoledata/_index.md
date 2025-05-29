---
title: LoadOptions.IgnoreOleData
linktitle: IgnoreOleData
articleTitle: IgnoreOleData
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen LoadOptions IgnoreOleData förbättrar din datahantering genom att låta dig kontrollera OLE-databearbetning. Optimera ditt arbetsflöde idag!
type: docs
weight: 70
url: /sv/net/aspose.words.loading/loadoptions/ignoreoledata/
---
## LoadOptions.IgnoreOleData property

Anger om OLE-data ska ignoreras.

```csharp
public bool IgnoreOleData { get; set; }
```

## Anmärkningar

Att ignorera OLE-data kan minska minnesförbrukningen och öka prestandan utan att data går förlorade i ett fall där destinationsformatet inte stöder OLE-objekt.

Standardvärdet är`falsk`.

## Exempel

Visar hur man ignorerar OLE-data vid inläsning.

```csharp
// Att ignorera OLE-data kan minska minnesförbrukningen och öka prestandan
// utan dataförlust i ett fall där destinationsformatet inte stöder OLE-objekt.
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Document doc = new Document(MyDir + "OLE objects.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.IgnoreOleData.docx");
```

### Se även

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
