---
title: Table.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Table VerticalAnchor för att optimera flytande tabellplacering. Lär dig hur du förbättrar layoutkontrollen med dess standardvärde för marginal.
type: docs
weight: 340
url: /sv/net/aspose.words.tables/table/verticalanchor/
---
## Table.VerticalAnchor property

Hämtar basobjektet från vilket den vertikala positioneringen av den flytande tabellen ska beräknas. Standardvärdet ärMargin .

```csharp
public RelativeVerticalPosition VerticalAnchor { get; set; }
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

* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
