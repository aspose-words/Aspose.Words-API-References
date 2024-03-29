---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: Aspose.Words för .NET
description: SaveOptions MemoryOptimization fast egendom. Hämtar eller ställer in värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen ärfalsk  i C#.
type: docs
weight: 100
url: /sv/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

Hämtar eller ställer in värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen är`falsk` .

```csharp
public bool MemoryOptimization { get; set; }
```

## Anmärkningar

Ställer in detta alternativ till`Sann` kan minska minnesförbrukningen avsevärt samtidigt som stora dokument sparas till priset av långsammare spartid.

## Exempel

Visar ett alternativ för att optimera minnesförbrukningen vid rendering av stora dokument till PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Ställ in egenskapen "MemoryOptimization" till "true" för att minska minnesutrymmet för stora dokuments lagringsåtgärder
// till priset av att operationens varaktighet ökar.
// Ställ in egenskapen "MemoryOptimization" till "false" för att spara dokumentet som en PDF-fil normalt.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
