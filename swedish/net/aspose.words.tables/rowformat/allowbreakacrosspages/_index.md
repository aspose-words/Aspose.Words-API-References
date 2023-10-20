---
title: RowFormat.AllowBreakAcrossPages
linktitle: AllowBreakAcrossPages
articleTitle: AllowBreakAcrossPages
second_title: Aspose.Words för .NET
description: RowFormat AllowBreakAcrossPages fast egendom. Sant om texten i en tabellrad tillåts delas över en sidbrytning i C#.
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

Visar hur du inaktiverar rader som delas över sidor för varje rad i en tabell.

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Ställ in egenskapen "AllowBreakAcrossPages" till "false" för att behålla raden
// i ett stycke om en tabell sträcker sig över två sidor, som delas upp längs den raden.
// Om raden är för stor för att få plats på en sida, kommer Microsoft Word att trycka ner den till nästa sida.
// Ställ in egenskapen "AllowBreakAcrossPages" på "true" för att tillåta att raden delas upp på två sidor.
foreach (Row row in table.OfType<Row>())
    row.RowFormat.AllowBreakAcrossPages = allowBreakAcrossPages;

doc.Save(ArtifactsDir + "Table.AllowBreakAcrossPages.docx");
```

### Se även

* class [RowFormat](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
