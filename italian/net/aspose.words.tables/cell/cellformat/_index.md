---
title: Cell.CellFormat
linktitle: CellFormat
articleTitle: CellFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà CellFormat della cella per accedere facilmente e personalizzare le opzioni di formattazione delle celle, per una presentazione migliore dei dati nelle tue applicazioni.
type: docs
weight: 20
url: /it/net/aspose.words.tables/cell/cellformat/
---
## Cell.CellFormat property

Fornisce accesso alle proprietà di formattazione della cella.

```csharp
public CellFormat CellFormat { get; }
```

## Esempi

Mostra come modificare la formattazione di una cella di una tabella.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

// Utilizzare la proprietà "CellFormat" di una cella per impostare la formattazione che modifica l'aspetto di quella cella.
firstCell.CellFormat.Width = 30;
firstCell.CellFormat.Orientation = TextOrientation.Downward;
firstCell.CellFormat.Shading.ForegroundPatternColor = Color.LightGreen;

doc.Save(ArtifactsDir + "Table.CellFormat.docx");
```

Mostra come combinare le righe di due tabelle in una.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

// Di seguito sono riportati due modi per ottenere una tabella da un documento.
// 1 - Dalla raccolta "Tabelle" di un nodo Corpo:
Table firstTable = doc.FirstSection.Body.Tables[0];

// 2 - Utilizzo del metodo "GetChild":
Table secondTable = (Table)doc.GetChild(NodeType.Table, 1, true);

// Aggiunge tutte le righe dalla tabella corrente a quella successiva.
while (secondTable.HasChildNodes)
    firstTable.Rows.Add(secondTable.FirstRow);

// Rimuove il contenitore della tabella vuota.
secondTable.Remove();

doc.Save(ArtifactsDir + "Table.CombineTables.docx");
```

Mostra come modificare il formato di righe e celle in una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("City");
builder.InsertCell();
builder.Write("Country");
builder.EndRow();
builder.InsertCell();
builder.Write("London");
builder.InsertCell();
builder.Write("U.K.");
builder.EndTable();

// Utilizzare la proprietà "RowFormat" della prima riga per modificare la formattazione
// del contenuto di tutte le celle in questa riga.
RowFormat rowFormat = table.FirstRow.RowFormat;
rowFormat.Height = 25;
rowFormat.Borders[BorderType.Bottom].Color = Color.Red;

// Utilizzare la proprietà "CellFormat" della prima cella nell'ultima riga per modificare la formattazione del contenuto di quella cella.
CellFormat cellFormat = table.LastRow.FirstCell.CellFormat;
cellFormat.Width = 100;
cellFormat.Shading.BackgroundPatternColor = Color.Orange;

doc.Save(ArtifactsDir + "Table.RowCellFormat.docx");
```

### Guarda anche

* class [CellFormat](../../cellformat/)
* class [Cell](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
