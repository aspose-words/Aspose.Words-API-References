---
title: PreferredWidth.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PreferredWidth Type, som definierar måttenheten för önskade breddvärden, vilket förbättrar din designprecision och flexibilitet.
type: docs
weight: 40
url: /sv/net/aspose.words.tables/preferredwidth/type/
---
## PreferredWidth.Type property

Hämtar måttenheten som används för detta önskade breddvärde.

```csharp
public PreferredWidthType Type { get; }
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

* enum [PreferredWidthType](../../preferredwidthtype/)
* class [PreferredWidth](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
