---
title: BuiltInDocumentProperties.LastPrinted
linktitle: LastPrinted
articleTitle: LastPrinted
second_title: Aspose.Words för .NET
description: BuiltInDocumentProperties LastPrinted fast egendom. Hämtar eller ställer in datumet när dokumentet senast skrevs ut i UTC i C#.
type: docs
weight: 150
url: /sv/net/aspose.words.properties/builtindocumentproperties/lastprinted/
---
## BuiltInDocumentProperties.LastPrinted property

Hämtar eller ställer in datumet när dokumentet senast skrevs ut i UTC.

```csharp
public DateTime LastPrinted { get; set; }
```

## Anmärkningar

För dokument som kommer från RTF-format returnerar denna egenskap den lokala tiden för senaste utskrift.

Om dokumentet aldrig skrevs ut kommer den här egenskapen att returnera DateTime.MinValue.

Aspose.Words uppdaterar inte den här egenskapen.

## Exempel

Visar hur man arbetar med dokumentegenskaper i kategorin "Ursprung".

```csharp
// Öppna ett dokument som vi har skapat och redigerat med Microsoft Word.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Följande inbyggda egenskaper innehåller information om skapandet och redigeringen av detta dokument.
// Vi kan högerklicka på det här dokumentet i Utforskaren och hitta
// dessa egenskaper via "Egenskaper" -> "Detaljer" -> "Ursprung" kategori.
// Fält som PRINTDATE och EDITTIME kan visa dessa värden i dokumentets brödtext.
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// Vi kan också ändra värden på inbyggda fastigheter.
properties.Company = "Doe Ltd.";
properties.Manager = "Jane Doe";
properties.Version = 5;
properties.RevisionNumber++;

// Microsoft Word uppdaterar följande egenskaper automatiskt när vi sparar dokumentet.
// För att använda dessa egenskaper med Aspose.Words måste vi ställa in värden för dem manuellt.
properties.LastSavedBy = "John Doe";
properties.LastSavedTime = DateTime.Now;

// Vi kan högerklicka på det här dokumentet i Utforskaren och hitta these properties in "Properties" -> "Details" -> "Origin".
doc.Save(ArtifactsDir + "DocumentProperties.Origin.docx");
```

### Se även

* class [BuiltInDocumentProperties](../)
* namnutrymme [Aspose.Words.Properties](../../../aspose.words.properties/)
* hopsättning [Aspose.Words](../../../)
