---
title: Table.AllowOverlap
second_title: Aspose.Words för .NET API Referens
description: Table fast egendom. Hämtar om en flytande tabell ska tillåta andra flytande objekt i document att överlappa dess omfattning när den visas. Standardvärdet ärSann .
type: docs
weight: 70
url: /sv/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

Hämtar om en flytande tabell ska tillåta andra flytande objekt i document att överlappa dess omfattning när den visas. Standardvärdet är`Sann` .

```csharp
public bool AllowOverlap { get; }
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

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../table/)
* hopsättning [Aspose.Words](../../../)


