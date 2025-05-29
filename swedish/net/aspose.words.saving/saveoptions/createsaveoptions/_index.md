---
title: SaveOptions.CreateSaveOptions
linktitle: CreateSaveOptions
articleTitle: CreateSaveOptions
second_title: Aspose.Words för .NET
description: Upptäck metoden CreateSaveOptions för att enkelt generera sparalternativ skräddarsydda för ditt önskade format, vilket förbättrar effektiviteten i din dokumenthantering.
type: docs
weight: 10
url: /sv/net/aspose.words.saving/saveoptions/createsaveoptions/
---
## CreateSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#createsaveoptions}

Skapar ett objekt för sparalternativ av en klass som är lämplig för det angivna sparformatet.

```csharp
public static SaveOptions CreateSaveOptions(SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| saveFormat | SaveFormat | Sparformatet för att skapa ett objekt för sparalternativ. |

### Returvärde

Ett objekt i en klass som härleds från[`SaveOptions`](../).

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)

---

## CreateSaveOptions(*string*) {#createsaveoptions_1}

Skapar ett objekt för spara alternativ av en klass som är lämplig för filändelsen som anges i det angivna filnamnet.

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Filnamnstillägget avgör vilken klassen för det sparade alternativobjektet som ska skapas. |

### Returvärde

Ett objekt i en klass som härleds från[`SaveOptions`](../).

## Exempel

Visar hur man ställer in en standardmall för dokument som inte har bifogade mallar.

```csharp
Document doc = new Document();

// Aktivera automatisk stiluppdatering, men bifoga inte ett malldokument.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Eftersom det inte finns något malldokument fanns det ingenstans i dokumentet att spåra stiländringar.
// Använd ett SaveOptions-objekt för att automatiskt ställa in en mall
// om ett dokument som vi sparar inte har ett.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Se även

* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
