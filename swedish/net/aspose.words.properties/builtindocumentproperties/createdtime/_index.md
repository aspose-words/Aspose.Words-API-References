---
title: BuiltInDocumentProperties.CreatedTime
linktitle: CreatedTime
articleTitle: CreatedTime
second_title: Aspose.Words för .NET
description: Upptäck funktionen BuiltInDocumentProperties CreatedTime för att enkelt komma åt och hantera ditt dokuments skapandedatum i UTC för förbättrad organisation.
type: docs
weight: 100
url: /sv/net/aspose.words.properties/builtindocumentproperties/createdtime/
---
## BuiltInDocumentProperties.CreatedTime property

Hämtar eller ställer in datum för dokumentets skapande i UTC.

```csharp
public DateTime CreatedTime { get; set; }
```

## Anmärkningar

För dokument som kommer från RTF-format returnerar den här egenskapen lokal tid på författarens dator vid tidpunkten för dokumentskapandet.

Aspose.Words uppdaterar inte den här egenskapen.

## Exempel

Visar hur man arbetar med dokumentegenskaper i kategorin "Ursprung".

```csharp
// Öppna ett dokument som vi har skapat och redigerat med Microsoft Word.
Document doc = new Document(MyDir + "Properties.docx");
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

// Följande inbyggda egenskaper innehåller information om skapandet och redigeringen av detta dokument.
// Vi kan högerklicka på det här dokumentet i Utforskaren och hitta
// dessa egenskaper via kategorin "Egenskaper" -> "Detaljer" -> "Ursprung".
// Fält som PRINTDATE och EDITTIME kan visa dessa värden i dokumentets brödtext.
Console.WriteLine($"Created using {properties.NameOfApplication}, on {properties.CreatedTime}");
Console.WriteLine($"Minutes spent editing: {properties.TotalEditingTime}");
Console.WriteLine($"Date/time last printed: {properties.LastPrinted}");
Console.WriteLine($"Template document: {properties.Template}");

// Vi kan också ändra värdena för inbyggda egenskaper.
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
