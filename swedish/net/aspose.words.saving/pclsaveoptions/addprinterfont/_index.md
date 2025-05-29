---
title: PclSaveOptions.AddPrinterFont
linktitle: AddPrinterFont
articleTitle: AddPrinterFont
second_title: Aspose.Words för .NET
description: Upptäck PclSaveOptions AddPrinterFont-metoden för att effektivt ladda upp och hantera skrivarfonter från tillverkare för förbättrad utskriftsprestanda.
type: docs
weight: 50
url: /sv/net/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions.AddPrinterFont method

Lägger till information om teckensnitt som laddas upp till skrivaren av tillverkaren.

```csharp
public void AddPrinterFont(string fontFullName, string fontPclName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fontFullName | String | Typsnittets fullständiga namn (t.ex. "Times New Roman Bold Italic"). |
| fontPclName | String | Namn på teckensnittet som används i Pcl-dokumentet. |

## Anmärkningar

Det finns 52 teckensnitt som ska byggas in i alla skrivare enligt Pcl-specifikationen. Tillverkare kan dock lägga till andra teckensnitt i sina enheter.

## Exempel

Visar hur man får en skrivare att ersätta alla förekomster av ett specifikt teckensnitt med ett annat teckensnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// När detta dokument skrivs ut använder skrivaren teckensnittet "Courier New"
// för att komma åt platser där vårt dokument använde teckensnittet "Courier".
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### Se även

* class [PclSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
