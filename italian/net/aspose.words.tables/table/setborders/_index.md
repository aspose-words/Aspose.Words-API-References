---
title: SetBorders
second_title: Aspose.Words per .NET API Reference
description: Imposta tutti i bordi della tabella sullo stile della linea sulla larghezza e sul colore specificati.
type: docs
weight: 420
url: /it/net/aspose.words.tables/table/setborders/
---
## Table.SetBorders method

Imposta tutti i bordi della tabella sullo stile della linea, sulla larghezza e sul colore specificati.

```csharp
public void SetBorders(LineStyle lineStyle, double lineWidth, Color color)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| lineStyle | LineStyle | Lo stile della linea da applicare. |
| lineWidth | Double | La larghezza della linea da impostare (in punti). |
| color | Color | Il colore da usare per il bordo. |

### Esempi

Mostra come formattare contemporaneamente tutti i bordi di una tabella.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Cancella tutti i bordi esistenti dalla tabella.
table.ClearBorders();

// Imposta una singola linea verde che serva da ogni bordo esterno e interno di questa tabella.
table.SetBorders(LineStyle.Single, 1.5, Color.Green);

doc.Save(ArtifactsDir + "Table.SetBorders.docx");
```

Mostra come applicare il colore del bordo e dell'ombreggiatura durante la creazione di una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Avvia una tabella e imposta un colore/spessore predefinito per i suoi bordi.
Table table = builder.StartTable();
table.SetBorders(LineStyle.Single, 2.0, Color.Black);

// Crea una riga con due celle con diversi colori di sfondo.
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.LightSkyBlue;
builder.Writeln("Row 1, Cell 1.");
builder.InsertCell();
builder.CellFormat.Shading.BackgroundPatternColor = Color.Orange;
builder.Writeln("Row 1, Cell 2.");
builder.EndRow();

// Ripristina la formattazione della cella per disabilitare i colori di sfondo
// imposta uno spessore del bordo personalizzato per tutte le nuove celle create dal builder,
// quindi costruisci una seconda riga.
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

* enum [LineStyle](../../../aspose.words/linestyle)
* class [Table](../../table)
* spazio dei nomi [Aspose.Words.Tables](../../table)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->