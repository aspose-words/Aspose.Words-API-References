---
title: BuiltInDocumentProperties.Template
linktitle: Template
articleTitle: Template
second_title: Aspose.Words för .NET
description: Upptäck mallfunktionen BuiltInDocumentProperties för att enkelt hantera dokumentets informationsnamn för förbättrad organisation och effektivitet.
type: docs
weight: 300
url: /sv/net/aspose.words.properties/builtindocumentproperties/template/
---
## BuiltInDocumentProperties.Template property

Hämtar eller anger dokumentmallens informationsnamn.

```csharp
public string Template { get; set; }
```

## Anmärkningar

I Microsoft Word är den här egenskapen endast i informationssyfte och innehåller vanligtvis bara mallens filnamn utan sökvägen.

Tom sträng betyder att dokumentet är kopplat till Normal-mallen.

För att hämta eller ange det faktiska namnet på den bifogade mallen, använd the [`AttachedTemplate`](../../../aspose.words/document/attachedtemplate/) egendom.

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
