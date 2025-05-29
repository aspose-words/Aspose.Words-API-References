---
title: Table.AllowOverlap
linktitle: AllowOverlap
articleTitle: AllowOverlap
second_title: Aspose.Words för .NET
description: Upptäck egenskapen Table AllowOverlap, som styr om flytande objekt kan överlappa din tabell. Förbättra layoutflexibiliteten för bättre dokumentpresentation.
type: docs
weight: 70
url: /sv/net/aspose.words.tables/table/allowoverlap/
---
## Table.AllowOverlap property

Hämtar om en flytande tabell ska tillåta andra flytande objekt i dokumentet att överlappa dess omfattning när den visas. Standardvärdet är`sann` .

```csharp
public bool AllowOverlap { get; }
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

* class [Table](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
