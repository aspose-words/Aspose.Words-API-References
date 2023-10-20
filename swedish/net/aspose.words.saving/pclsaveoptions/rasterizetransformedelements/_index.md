---
title: PclSaveOptions.RasterizeTransformedElements
linktitle: RasterizeTransformedElements
articleTitle: RasterizeTransformedElements
second_title: Aspose.Words för .NET
description: PclSaveOptions RasterizeTransformedElements fast egendom. Hämtar eller ställer in ett värde som bestämmer om komplexa transformerade element ska rastreras innan de sparas i PCLdokument. Standard ärSann  i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Hämtar eller ställer in ett värde som bestämmer om komplexa transformerade element ska rastreras innan de sparas i PCL-dokument. Standard är`Sann` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

## Anmärkningar

PCL stöder inte någon form av transformationer som används av Aspose Words. T.ex. roterade, sneda bilder och texturpenslar. För att korrekt rendera sådana element används rasteriseringsprocess, dvs. spara till bild och klippning. Denna process kan ta ytterligare tid och minne. Om flaggan är inställd på`falsk` , visst innehåll i utdata kan vara annorlunda jämfört med källdokumentet.

## Exempel

Visar hur man rastrar komplexa element samtidigt som ett dokument sparas till PCL.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PclSaveOptions saveOptions = new PclSaveOptions
{
    SaveFormat = SaveFormat.Pcl,
    RasterizeTransformedElements = true
};

doc.Save(ArtifactsDir + "PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

### Se även

* class [PclSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
