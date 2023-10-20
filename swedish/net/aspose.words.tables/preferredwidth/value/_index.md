---
title: PreferredWidth.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words för .NET
description: PreferredWidth Value fast egendom. Hämtar önskat breddvärde. Måttenheten anges iType egenskap i C#.
type: docs
weight: 50
url: /sv/net/aspose.words.tables/preferredwidth/value/
---
## PreferredWidth.Value property

Hämtar önskat breddvärde. Måttenheten anges i[`Type`](../type/) egenskap.

```csharp
public double Value { get; }
```

## Exempel

Visar hur man verifierar den föredragna breddtypen och värdet för en tabellcell.

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
