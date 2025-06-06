---
title: Table.SetBorders
linktitle: SetBorders
articleTitle: SetBorders
second_title: Aspose.Words per .NET
description: Personalizza le tue tabelle senza sforzo con il metodo SetBorders, regolando lo stile, la larghezza e il colore delle linee per un aspetto curato e professionale.
type: docs
weight: 440
url: /it/net/aspose.words.tables/table/setborders/
---
## Table.SetBorders method

Imposta tutti i bordi della tabella sullo stile di linea, la larghezza e il colore specificati.

```csharp
public void SetBorders(LineStyle lineStyle, double lineWidth, Color color)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| lineStyle | LineStyle | Stile della linea da applicare. |
| lineWidth | Double | Larghezza della linea da impostare (in punti). |
| color | Color | Il colore da usare per il bordo. |

## Esempi

Mostra come formattare tutti i bordi di una tabella contemporaneamente.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Cancella tutti i bordi esistenti dalla tabella.
table.ClearBorders();

// Imposta una singola linea verde che funga da bordo esterno e interno per ogni tabella.
table.SetBorders(LineStyle.Single, 1.5, Color.Green);

doc.Save(ArtifactsDir + "Table.SetBorders.docx");
```

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

* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
