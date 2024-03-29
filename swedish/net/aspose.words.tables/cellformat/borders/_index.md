---
title: CellFormat.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words för .NET
description: CellFormat Borders fast egendom. Får samling av cellens kanter i C#.
type: docs
weight: 10
url: /sv/net/aspose.words.tables/cellformat/borders/
---
## CellFormat.Borders property

Får samling av cellens kanter.

```csharp
public BorderCollection Borders { get; }
```

## Exempel

Visar hur man kombinerar raderna från två tabeller till en.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Nedan finns två sätt att hämta en tabell från ett dokument.
// 1 - Från samlingen "Tables" för en Body-nod:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Med "GetChild"-metoden:
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Lägg till alla rader från den aktuella tabellen till nästa.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Ta bort den tomma bordsbehållaren.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Se även

* class [BorderCollection](../../../aspose.words/bordercollection/)
* class [CellFormat](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
