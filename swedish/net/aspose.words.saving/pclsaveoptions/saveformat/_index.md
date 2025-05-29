---
title: PclSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PclSaveOptions SaveFormat för att enkelt spara dokument i PCL-format, vilket säkerställer kompatibilitet och högkvalitativa resultat för dina projekt.
type: docs
weight: 40
url: /sv/net/aspose.words.saving/pclsaveoptions/saveformat/
---
## PclSaveOptions.SaveFormat property

Anger formatet som dokumentet sparas i om detta objekt för sparade alternativ används. Kan endast varaPcl .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PclSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
