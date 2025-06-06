---
title: CellFormat.PreferredWidth
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words per .NET
description: Scopri la proprietà CellFormat PreferredWidth per personalizzare facilmente la larghezza delle celle e ottenere un layout e un design ottimali nei tuoi fogli di calcolo. Migliora la presentazione dei tuoi dati!
type: docs
weight: 80
url: /it/net/aspose.words.tables/cellformat/preferredwidth/
---
## CellFormat.PreferredWidth property

Restituisce o imposta la larghezza preferita della cella.

```csharp
public PreferredWidth PreferredWidth { get; set; }
```

## Osservazioni

La larghezza preferita (insieme all'opzione Adattamento automatico della tabella) determina come l'algoritmo di layout della tabella calcola la larghezza effettiva della cella. Il layout della tabella può essere eseguito da Aspose.Words al momento del salvataggio del documento o da Microsoft Word al momento della visualizzazione.

La larghezza preferita può essere specificata in punti o in percentuale. La larghezza preferita può anche essere specificata come "auto", il che significa che non viene specificata alcuna larghezza preferita.

Il valore predefinito è[`Auto`](../../preferredwidth/auto/).

## Esempi

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

* class [PreferredWidth](../../preferredwidth/)
* class [CellFormat](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
