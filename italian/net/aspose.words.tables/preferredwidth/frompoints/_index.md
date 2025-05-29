---
title: PreferredWidth.FromPoints
linktitle: FromPoints
articleTitle: FromPoints
second_title: Aspose.Words per .NET
description: Scopri il metodo PreferredWidth FromPoints per creare una nuova istanza con una larghezza definita in punti, migliorando così la precisione e l'efficienza della progettazione.
type: docs
weight: 30
url: /it/net/aspose.words.tables/preferredwidth/frompoints/
---
## PreferredWidth.FromPoints method

Un metodo di creazione che restituisce una nuova istanza che rappresenta una larghezza preferita specificata utilizzando un numero di punti.

```csharp
public static PreferredWidth FromPoints(double points)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| points | Double | Il valore deve essere compreso tra 0 e 22 pollici (22 * 72 punti). |

## Esempi

Mostra come utilizzare gli strumenti di conversione delle unità specificando la larghezza preferita per una cella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(ConvertUtil.InchToPoint(3));
builder.InsertCell();

Assert.AreEqual(216.0d, table.FirstRow.FirstCell.CellFormat.PreferredWidth.Value);
```

Mostra come impostare una larghezza preferita per le celle di una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Table table = builder.StartTable();

// Esistono due modi per applicare la classe "PreferredWidth" alle celle della tabella.
// 1 - Imposta una larghezza preferita assoluta in base ai punti:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(40);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightYellow;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

// 2 - Imposta una larghezza preferita relativa in base alla percentuale della larghezza della tabella:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Una cella per la quale non è stata specificata una larghezza preferita occuperà il resto dello spazio disponibile.
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;

// Ogni configurazione della proprietà "PreferredWidth" crea un nuovo oggetto.
Assert.AreNotEqual(table.FirstRow.Cells[1].CellFormat.PreferredWidth.GetHashCode(),
    builder.CellFormat.PreferredWidth.GetHashCode());

builder.CellFormat.Shading.BackgroundPatternColor = Color.LightGreen;
builder.Writeln("Automatically sized cell.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
```

### Guarda anche

* class [PreferredWidth](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
