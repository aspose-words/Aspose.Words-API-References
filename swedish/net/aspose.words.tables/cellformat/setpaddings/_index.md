---
title: CellFormat.SetPaddings
linktitle: SetPaddings
articleTitle: SetPaddings
second_title: Aspose.Words för .NET
description: Upptäck CellFormat SetPaddings-metoden för att anpassa cellavståndet i punkter, vilket förbättrar din layout för förbättrad läsbarhet och design.
type: docs
weight: 170
url: /sv/net/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat.SetPaddings method

Anger mängden utrymme (i punkter) som ska läggas till vänster/överst/höger/nederst i cellens innehåll.

```csharp
public void SetPaddings(double leftPadding, double topPadding, double rightPadding, 
    double bottomPadding)
```

## Exempel

Visar hur man fyller ut innehållet i en cell med blanksteg.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ange ett utfyllnadsavstånd (i punkter) mellan kantlinjen och textinnehållet
 // för varje tabellcell vi skapar med dokumentbyggaren.
builder.CellFormat.SetPaddings(5, 10, 40, 50);

// Skapa en tabell med en cell vars innehåll kommer att ha utfyllnad med blanktecken.
builder.StartTable();
builder.InsertCell();
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "CellFormat.Padding.docx");
```

### Se även

* class [CellFormat](../)
* namnutrymme [Aspose.Words.Tables](../../../aspose.words.tables/)
* hopsättning [Aspose.Words](../../../)
