---
title: CellFormat.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words för .NET
description: Upptäck CellFormat ClearFormatting-metoden för att enkelt återställa cellformat till standardinställningarna utan att ändra cellbredden. Förbättra effektiviteten i ditt kalkylblad!
type: docs
weight: 160
url: /sv/net/aspose.words.tables/cellformat/clearformatting/
---
## CellFormat.ClearFormatting method

Återställer till standardcellformatering. Ändrar inte cellens bredd.

```csharp
public void ClearFormatting()
```

## Exempel

Visar hur man kombinerar rader från två tabeller till en.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Nedan följer två sätt att hämta en tabell från ett dokument.
// 1 - Från samlingen "Tabeller" i en Body-nod:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Använda metoden "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Lägger till alla rader från den aktuella tabellen till nästa.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Ta bort den tomma tabellbehållaren.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

### Se även

* class [CellFormat](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
