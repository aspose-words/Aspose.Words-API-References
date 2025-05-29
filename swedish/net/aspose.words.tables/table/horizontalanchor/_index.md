---
title: Table.HorizontalAnchor
linktitle: HorizontalAnchor
articleTitle: HorizontalAnchor
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Table HorizontalAnchor för att optimera placeringen av flytande tabeller. Anpassa enkelt horisontell justering för förbättrad layoutkontroll.
type: docs
weight: 170
url: /sv/net/aspose.words.tables/table/horizontalanchor/
---
## Table.HorizontalAnchor property

Hämtar basobjektet från vilket den horisontella positioneringen av den flytande tabellen ska beräknas. Standardvärdet ärColumn .

```csharp
public RelativeHorizontalPosition HorizontalAnchor { get; set; }
```

## Exempel

Visar hur man arbetar med egenskaper för flytande tabeller.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // Endast marginal, sida och kolumn är tillgängliga i RelativeHorizontalPosition för HorizontalAnchor-sättaren.
    // ArgumentException kommer att utlösas för alla andra värden.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Endast marginal, sida och stycke tillgängliga i RelativeVerticalPosition för VerticalAnchor-inställaren.
    // ArgumentException kommer att utlösas för alla andra värden.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Se även

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
