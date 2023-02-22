---
title: Table.VerticalAnchor
second_title: Aspose.Words för .NET API Referens
description: Table fast egendom. Hämtar basobjektet från vilket den vertikala positioneringen av flytande tabell ska beräknas. Standardvärdet ärMargin .
type: docs
weight: 340
url: /sv/net/aspose.words.tables/table/verticalanchor/
---
## Table.VerticalAnchor property

Hämtar basobjektet från vilket den vertikala positioneringen av flytande tabell ska beräknas. Standardvärdet ärMargin .

```csharp
public RelativeVerticalPosition VerticalAnchor { get; set; }
```

### Exempel

Visar hur man arbetar med egenskaper för flytande tabeller.

```csharp
Document doc = new Document(MyDir + "Table wrapped by text.docx");

Table table = doc.FirstSection.Body.Tables[0];

if (table.TextWrapping == TextWrapping.Around)
{
    Assert.AreEqual(RelativeHorizontalPosition.Margin, table.HorizontalAnchor);
    Assert.AreEqual(RelativeVerticalPosition.Paragraph, table.VerticalAnchor);
    Assert.AreEqual(false, table.AllowOverlap);

    // Endast Marginal, Sida, Kolumn tillgängliga i RelativeHorizontalPosition för HorizontalAnchor Setter.
    // ArgumentException kommer att kastas för alla andra värden.
    table.HorizontalAnchor = RelativeHorizontalPosition.Column;

    // Endast Marginal, Sida, Paragraph tillgängliga i RelativeVerticalPosition för VerticalAnchor Setter.
    // ArgumentException kommer att kastas för alla andra värden.
    table.VerticalAnchor = RelativeVerticalPosition.Page;
}
```

### Se även

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../table/)
* hopsättning [Aspose.Words](../../../)


