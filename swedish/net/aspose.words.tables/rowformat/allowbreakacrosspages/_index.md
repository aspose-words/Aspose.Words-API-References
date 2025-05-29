---
title: RowFormat.AllowBreakAcrossPages
linktitle: AllowBreakAcrossPages
articleTitle: AllowBreakAcrossPages
second_title: Aspose.Words för .NET
description: Upptäck egenskapen RowFormat AllowBreakAcrossPages, aktivera sömlöst textflöde i tabellrader över sidbrytningar för förbättrad läsbarhet och presentation.
type: docs
weight: 10
url: /sv/net/aspose.words.tables/rowformat/allowbreakacrosspages/
---
## RowFormat.AllowBreakAcrossPages property

Sant om texten i en tabellrad tillåts delas över en sidbrytning.

```csharp
public bool AllowBreakAcrossPages { get; set; }
```

## Exempel

Visar hur man inaktiverar radbrytning över sidor för varje rad i en tabell.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Sätt egenskapen "AllowBreakAcrossPages" till "false" för att behålla raden
// i ett stycke om en tabell sträcker sig över två sidor, som bryts upp längs den raden.
// Om raden är för stor för att få plats på en sida, flyttas den till nästa sida i Microsoft Word.
// Sätt egenskapen "AllowBreakAcrossPages" till "true" för att tillåta att raden delas upp över två sidor.
foreach (Row row in table)
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### Se även

* class [RowFormat](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
