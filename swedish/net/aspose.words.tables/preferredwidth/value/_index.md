---
title: PreferredWidth.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PreferredWidth Value för att enkelt komma åt och anpassa din önskade bredd. Förbättra din design med exakta mått idag!
type: docs
weight: 50
url: /sv/net/aspose.words.tables/preferredwidth/value/
---
## PreferredWidth.Value property

Hämtar önskat breddvärde. Måttenheten anges i[`Type`](../type/) egendom.

```csharp
public double Value { get; }
```

## Exempel

Visar hur man verifierar önskad breddtyp och värde för en tabellcell.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### Se även

* class [PreferredWidth](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
