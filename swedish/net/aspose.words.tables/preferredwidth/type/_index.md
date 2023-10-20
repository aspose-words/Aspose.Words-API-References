---
title: PreferredWidth.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words för .NET
description: PreferredWidth Type fast egendom. Hämtar måttenheten som används för detta föredragna breddvärde i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.tables/preferredwidth/type/
---
## PreferredWidth.Type property

Hämtar måttenheten som används för detta föredragna breddvärde.

```csharp
public PreferredWidthType Type { get; }
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

* enum [PreferredWidthType](../../preferredwidthtype/)
* class [PreferredWidth](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
