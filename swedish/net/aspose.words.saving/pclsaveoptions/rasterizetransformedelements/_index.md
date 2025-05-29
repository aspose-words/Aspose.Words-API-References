---
title: PclSaveOptions.RasterizeTransformedElements
linktitle: RasterizeTransformedElements
articleTitle: RasterizeTransformedElements
second_title: Aspose.Words för .NET
description: Styr rasterisering av komplexa element i PCL-dokument med PclSaveOptions. Hantera enkelt bildkvalitet och filstorlek för optimala resultat.
type: docs
weight: 30
url: /sv/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

Hämtar eller anger ett värde som avgör om komplexa transformerade element ska rastreras innan de sparas till PCL-dokumentet. Standard är`sann` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

## Anmärkningar

PCL stöder inte vissa typer av transformationer som används av Aspose Words. T.ex. roterade, sneda bilder och texturpenslar. För att korrekt rendera sådana element används rasteriseringsprocessen, dvs. spara till bild och klippning. Denna process kan ta ytterligare tid och minne. Om flaggan är inställd på`falsk` , en del innehåll i utdata kan skilja sig jämfört med källdokumentet.

## Exempel

Visar hur man rastrerar komplexa element när man sparar ett dokument till PCL.

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
