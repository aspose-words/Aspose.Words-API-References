---
title: PreferredWidth Class
linktitle: PreferredWidth
articleTitle: PreferredWidth
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Tables.PreferredWidth, la soluzione ideale per definire la larghezza ottimale di tabelle e celle con precisione e flessibilità. Migliora il layout dei tuoi documenti oggi stesso!
type: docs
weight: 7140
url: /it/net/aspose.words.tables/preferredwidth/
---
## PreferredWidth class

Rappresenta un valore e la sua unità di misura utilizzata per specificare la larghezza preferita di una tabella o di una cella.

Per saperne di più, visita il[Lavorare con le tabelle](https://docs.aspose.com/words/net/working-with-tables/) articolo di documentazione.

```csharp
public sealed class PreferredWidth
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Type](../../aspose.words.tables/preferredwidth/type/) { get; } | Ottiene l'unità di misura utilizzata per questo valore di larghezza preferito. |
| [Value](../../aspose.words.tables/preferredwidth/value/) { get; } | Ottiene il valore di larghezza preferito. L'unità di misura è specificata in[`Type`](./type/) proprietà. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| static [FromPercent](../../aspose.words.tables/preferredwidth/frompercent/)(*double*) | Un metodo di creazione che restituisce una nuova istanza che rappresenta una larghezza preferita specificata come percentuale. |
| static [FromPoints](../../aspose.words.tables/preferredwidth/frompoints/)(*double*) | Un metodo di creazione che restituisce una nuova istanza che rappresenta una larghezza preferita specificata utilizzando un numero di punti. |
| override [Equals](../../aspose.words.tables/preferredwidth/equals/#equals_1)(*object*) | Determina se l'oggetto specificato ha un valore uguale all'oggetto corrente. |
| [Equals](../../aspose.words.tables/preferredwidth/equals/#equals)(*PreferredWidth*) | Determina se il valore specificato`PreferredWidth` ha un valore uguale a quello attuale`PreferredWidth` . |
| override [GetHashCode](../../aspose.words.tables/preferredwidth/gethashcode/)() | Serve come funzione hash per questo tipo. |
| override [ToString](../../aspose.words.tables/preferredwidth/tostring/)() | Restituisce una stringa di facile utilizzo che visualizza il valore di questo oggetto. |

## Campi

| Nome | Descrizione |
| --- | --- |
| static readonly [Auto](../../aspose.words.tables/preferredwidth/auto/) | Restituisce un'istanza che rappresenta il valore "larghezza preferita non specificata". |

## Osservazioni

La larghezza preferita può essere specificata come percentuale, numero di punti o un valore speciale "nessuno/automatico".

Le istanze di questa classe sono immutabili.

## Esempi

Mostra come impostare una tabella in modo che si adatti automaticamente al 50% della larghezza della pagina.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell #1");
builder.InsertCell();
builder.Write("Cell #2");
builder.InsertCell();
builder.Write("Cell #3");

table.PreferredWidth = PreferredWidth.FromPercent(50);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
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

* spazio dei nomi [Aspose.Words.Tables](../../aspose.words.tables/)
* assemblea [Aspose.Words](../../)
