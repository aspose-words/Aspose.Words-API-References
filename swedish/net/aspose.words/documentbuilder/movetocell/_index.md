---
title: DocumentBuilder.MoveToCell
second_title: Aspose.Words för .NET API Referens
description: DocumentBuilder metod. Flyttar markören till en tabellcell i det aktuella avsnittet.
type: docs
weight: 510
url: /sv/net/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder.MoveToCell method

Flyttar markören till en tabellcell i det aktuella avsnittet.

```csharp
public void MoveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| tableIndex | Int32 | Indexet för tabellen att flytta till. |
| rowIndex | Int32 | Indexet för raden i tabellen. |
| columnIndex | Int32 | Indexet för kolumnen i tabellen. |
| characterIndex | Int32 | Indexet för tecknet inuti cellen. Ett negativt värde låter dig ange en position från slutet av cellen. Använd -1 för att flytta till slutet av cellen. |

### Anmärkningar

Navigeringen utförs i den aktuella berättelsen i det aktuella avsnittet.

För indexparametrarna, när index är större än eller lika med 0, anger det ett index from början med 0 som det första elementet. När index är mindre än 0, specificerade det ett index från slutet med -1 som det sista elementet.

### Exempel

Visar hur man flyttar en dokumentbyggares markör till en cell i en tabell.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa en tom 2x2-tabell.
builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndRow();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

// Eftersom vi har avslutat tabellen med EndTable-metoden,
// dokumentbyggarens markör är för närvarande utanför tabellen.
// Den här markören har samma funktion som Microsoft Words blinkande textmarkör.
// Det kan också flyttas till en annan plats i dokumentet med hjälp av byggarens MoveTo-metoder.
// Vi kan flytta markören tillbaka in i tabellen till en specifik cell.
builder.MoveToCell(0, 1, 1, 0);
builder.Write("Column 2, cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.MoveToCell.docx");
```

### Se även

* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../documentbuilder/)
* hopsättning [Aspose.Words](../../../)


