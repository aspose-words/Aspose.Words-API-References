---
title: CellFormat.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words för .NET
description: Upptäck egenskapen CellFormat Borders för att komma åt och anpassa cellkantsamlingar för förbättrad kalkylbladsdesign och funktionalitet.
type: docs
weight: 10
url: /sv/net/aspose.words.tables/cellformat/borders/
---
## CellFormat.Borders property

Hämtar en samling av cellens kantlinjer.

```csharp
public BorderCollection Borders { get; }
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

* class [BorderCollection](../../../aspose.words/bordercollection/)
* class [CellFormat](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
