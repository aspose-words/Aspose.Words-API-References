---
title: BorderCollection.Right
linktitle: Right
articleTitle: Right
second_title: Aspose.Words per .NET
description: Scopri BorderCollection Right per un controllo preciso dei bordi nei tuoi progetti. Migliora i tuoi layout con un bordo perfetto ogni volta!
type: docs
weight: 100
url: /it/net/aspose.words/bordercollection/right/
---
## BorderCollection.Right property

Ottiene il bordo giusto.

```csharp
public Border Right { get; }
```

## Esempi

Mostra come applicare i colori dei bordi e delle ombreggiature durante la creazione di una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Avvia una tabella e imposta un colore/spessore predefinito per i suoi bordi.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Crea una riga con due celle con colori di sfondo diversi.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Reimposta la formattazione della cella per disabilitare i colori di sfondo
// imposta uno spessore del bordo personalizzato per tutte le nuove celle create dal builder,
// quindi crea una seconda riga.
builder.CellFormat.ClearFormatting();
builder.CellFormat.Borders.Left.LineWidth = 4.0;
builder.CellFormat.Borders.Right.LineWidth = 4.0;
builder.CellFormat.Borders.Top.LineWidth = 4.0;
builder.CellFormat.Borders.Bottom.LineWidth = 4.0;

builder.InsertCell();
builder.Writeln("Row 2, Cell 1.");
builder.InsertCell();
builder.Writeln("Row 2, Cell 2.");

doc.Save(ArtifactsDir + "DocumentBuilder.TableBordersAndShading.docx");
```

### Guarda anche

* class [Border](../../border/)
* class [BorderCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
