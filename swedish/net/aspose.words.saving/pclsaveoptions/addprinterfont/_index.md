---
title: PclSaveOptions.AddPrinterFont
linktitle: AddPrinterFont
articleTitle: AddPrinterFont
second_title: Aspose.Words för .NET
description: PclSaveOptions AddPrinterFont metod. Lägger till information om teckensnitt som laddas upp till skrivaren av tillverkaren i C#.
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
| fontPclName | String | Namn på typsnittet som används i Pcl-dokument. |

## Anmärkningar

Det finns 52 typsnitt som ska byggas in i vilken skrivare som helst enligt Pcl-specifikationen. Tillverkarna kan dock lägga till några andra typsnitt till sina enheter.

## Exempel

Visar hur man får en skrivare att ersätta alla instanser av ett specifikt teckensnitt med ett annat teckensnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Courier";
builder.Write("Hello world!");

PclSaveOptions saveOptions = new PclSaveOptions();
saveOptions.AddPrinterFont("Courier New", "Courier");

// När du skriver ut detta dokument kommer skrivaren att använda teckensnittet "Courier New".
// för att komma åt platser där vårt dokument använde typsnittet "Courier".
doc.Save(ArtifactsDir + "PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

### Se även

* class [PclSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
