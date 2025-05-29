---
title: BuiltInDocumentProperties.Version
linktitle: Version
articleTitle: Version
second_title: Aspose.Words för .NET
description: Upptäck egenskapen BuiltInDocumentProperties Version, som visar appversionen som skapade ditt dokument. Förbättra din dokumenthantering idag!
type: docs
weight: 350
url: /sv/net/aspose.words.properties/builtindocumentproperties/version/
---
## BuiltInDocumentProperties.Version property

Representerar versionsnumret för det program som skapade dokumentet.

```csharp
public int Version { get; set; }
```

## Anmärkningar

När ett dokument skapades med Microsoft Word representerar den höga 16-bitarsvärdet huvudversionen och den låga 16-bitarsvärdet byggnumret.

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
