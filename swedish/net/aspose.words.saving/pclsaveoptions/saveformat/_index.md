---
title: PclSaveOptions.SaveFormat
second_title: Aspose.Words för .NET API Referens
description: PclSaveOptions fast egendom. Anger formatet som dokumentet kommer att sparas i om detta sparaalternativobjekt används. Kan endastPcl .
type: docs
weight: 40
url: /sv/net/aspose.words.saving/pclsaveoptions/saveformat/
---
## PclSaveOptions.SaveFormat property

Anger formatet som dokumentet kommer att sparas i om detta sparaalternativ-objekt används. Kan endastPcl .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Exempel

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PclSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../pclsaveoptions/)
* hopsättning [Aspose.Words](../../../)


