---
title: PreferredWidth.Equals
second_title: Aspose.Words per .NET API Reference
description: PreferredWidth metodo. Determina se il valore PreferredWidth specificato è uguale al valore PreferredWidth corrente.
type: docs
weight: 60
url: /it/net/aspose.words.tables/preferredwidth/equals/
---
## Equals(PreferredWidth) {#equals}

Determina se il valore PreferredWidth specificato è uguale al valore PreferredWidth corrente.

```csharp
public bool Equals(PreferredWidth other)
```

### Esempi

Mostra come impostare una larghezza preferita per le celle della tabella.

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

// 2 - Imposta una larghezza relativa preferita in base alla percentuale della larghezza della tabella:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Una cella senza una larghezza preferita specificata occuperà il resto dello spazio disponibile.
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
* spazio dei nomi [Aspose.Words.Tables](../../preferredwidth/)
* assemblea [Aspose.Words](../../../)

---

## Equals(object) {#equals_1}

Determina se l'oggetto specificato è uguale in valore all'oggetto corrente.

```csharp
public override bool Equals(object obj)
```

### Esempi

Mostra come impostare una larghezza preferita per le celle della tabella.

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

// 2 - Imposta una larghezza relativa preferita in base alla percentuale della larghezza della tabella:
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPercent(20);
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightBlue;
builder.Writeln($"Cell with a width of {builder.CellFormat.PreferredWidth}.");

builder.InsertCell();

// Una cella senza una larghezza preferita specificata occuperà il resto dello spazio disponibile.
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
* spazio dei nomi [Aspose.Words.Tables](../../preferredwidth/)
* assemblea [Aspose.Words](../../../)


