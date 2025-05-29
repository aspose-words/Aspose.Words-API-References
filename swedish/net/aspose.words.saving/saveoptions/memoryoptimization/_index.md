---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: Aspose.Words för .NET
description: Förbättra dokumentprestanda med egenskapen MemoryOptimization i SaveOptions. Kontrollera minnesanvändningen innan du sparar, vilket ökar effektiviteten och hastigheten.
type: docs
weight: 100
url: /sv/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

Hämtar eller anger värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen är`falsk` .

```csharp
public bool MemoryOptimization { get; set; }
```

## Anmärkningar

Ställer in det här alternativet på`sann` kan minska minnesförbrukningen avsevärt samtidigt som stora dokument sparas på bekostnad av långsammare spartid.

## Exempel

Visar ett alternativ för att optimera minnesförbrukningen vid rendering av stora dokument till PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Sätt egenskapen "MemoryOptimization" till "true" för att minska minnesåtgången för att spara stora dokument
// på bekostnad av att öka operationens varaktighet.
// Sätt egenskapen "MemoryOptimization" till "false" för att spara dokumentet som en PDF normalt.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
