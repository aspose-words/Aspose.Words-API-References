---
title: Shading Class
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Shading, progettata per migliorare i tuoi documenti con attributi di ombreggiatura personalizzabili, per un aspetto professionale.
type: docs
weight: 6820
url: /it/net/aspose.words/shading/
---
## Shading class

Contiene gli attributi di ombreggiatura per un oggetto.

Per saperne di più, visita il[Programmazione con documenti](https://docs.aspose.com/words/net/programming-with-documents/) articolo di documentazione.

```csharp
public class Shading : InternableComplexAttr
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BackgroundPatternColor](../../aspose.words/shading/backgroundpatterncolor/) { get; set; } | Ottiene o imposta il colore applicato allo sfondo del`Shading` oggetto. |
| [BackgroundPatternThemeColor](../../aspose.words/shading/backgroundpatternthemecolor/) { get; set; } | Ottiene o imposta il colore del tema del pattern di sfondo nello schema di colori applicato associato a questo`Shading` oggetto. |
| [BackgroundTintAndShade](../../aspose.words/shading/backgroundtintandshade/) { get; set; } | Ottiene o imposta un valore double che schiarisce o scurisce il colore del tema di sfondo. |
| [ForegroundPatternColor](../../aspose.words/shading/foregroundpatterncolor/) { get; set; } | Ottiene o imposta il colore applicato al primo piano dell'`Shading` oggetto. |
| [ForegroundPatternThemeColor](../../aspose.words/shading/foregroundpatternthemecolor/) { get; set; } | Ottiene o imposta il colore del tema del motivo in primo piano nello schema di colori applicato associato a questo`Shading` oggetto. |
| [ForegroundTintAndShade](../../aspose.words/shading/foregroundtintandshade/) { get; set; } | Ottiene o imposta un valore double che schiarisce o scurisce un colore del tema in primo piano. |
| [Texture](../../aspose.words/shading/texture/) { get; set; } | Ottiene o imposta la trama dell'ombreggiatura. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ClearFormatting](../../aspose.words/shading/clearformatting/)() | Rimuove l'ombreggiatura dall'oggetto. |
| override [Equals](../../aspose.words/shading/equals/#equals_1)(*object*) | Determina se l'oggetto specificato ha un valore uguale all'oggetto corrente. |
| [Equals](../../aspose.words/shading/equals/#equals)(*Shading*) | Determina se il valore specificato`Shading` ha un valore uguale a quello attuale`Shading` . |
| override [GetHashCode](../../aspose.words/shading/gethashcode/)() | Serve come funzione hash per questo tipo. |

## Esempi

Mostra come decorare il testo con bordi e ombreggiature.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
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

* class [InternableComplexAttr](../internablecomplexattr/)
* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
