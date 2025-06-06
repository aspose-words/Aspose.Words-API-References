---
title: TextOrientation Enum
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.TextOrientation per controllare facilmente l'allineamento del testo nelle celle delle tabelle e nelle cornici di testo, migliorando la presentazione e la leggibilità del documento.
type: docs
weight: 7280
url: /it/net/aspose.words/textorientation/
---
## TextOrientation enumeration

Specifica l'orientamento del testo su una pagina, in una cella di tabella o in una cornice di testo.

```csharp
public enum TextOrientation
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Horizontal | `0` | Il testo è disposto orizzontalmente (lr-tb). |
| Downward | `1` | Il testo viene ruotato di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl). |
| Upward | `3` | Il testo viene ruotato di 90 gradi verso sinistra per apparire dal basso verso l'alto (bt-lr). |
| HorizontalRotatedFarEast | `4` | Il testo è disposto orizzontalmente, ma i caratteri dell'Estremo Oriente sono ruotati di 90 gradi verso sinistra (lr-tb-v). |
| VerticalFarEast | `5` | I caratteri dell'Estremo Oriente appaiono in verticale, il resto del testo è ruotato di 90 gradi verso destra per apparire dall'alto verso il basso (tb-rl-v). |
| VerticalRotatedFarEast | `7` | I caratteri dell'Estremo Oriente appaiono in verticale, il resto del testo viene ruotato di 90 gradi verso destra per apparire dall'alto verso il basso verticalmente, quindi da sinistra a destra orizzontalmente (tb-lr-v). |

## Esempi

Mostra come creare una tabella formattata 2x2.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.VerticalAlignment = CellVerticalAlignment.Center;
builder.Write("Row 1, cell 1.");
builder.InsertCell();
builder.Write("Row 1, cell 2.");
builder.EndRow();

// Durante la creazione della tabella, il generatore di documenti applicherà i valori correnti delle proprietà RowFormat/CellFormat
// alla riga/cella corrente in cui si trova il cursore e a tutte le nuove righe/celle man mano che vengono create.
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[0].CellFormat.VerticalAlignment);
Assert.AreEqual(CellVerticalAlignment.Center, table.Rows[0].Cells[1].CellFormat.VerticalAlignment);

builder.InsertCell();
builder.RowFormat.Height = 100;
builder.RowFormat.HeightRule = HeightRule.Exactly;
builder.CellFormat.Orientation = TextOrientation.Upward;
builder.Write("Row 2, cell 1.");
builder.InsertCell();
builder.CellFormat.Orientation = TextOrientation.Downward;
builder.Write("Row 2, cell 2.");
builder.EndRow();
builder.EndTable();

// Le righe e le celle aggiunte in precedenza non vengono retroattivamente influenzate dalle modifiche apportate alla formattazione del builder.
Assert.AreEqual(0, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);
Assert.AreEqual(100, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);
Assert.AreEqual(TextOrientation.Upward, table.Rows[1].Cells[0].CellFormat.Orientation);
Assert.AreEqual(TextOrientation.Downward, table.Rows[1].Cells[1].CellFormat.Orientation);

doc.Save(ArtifactsDir + "DocumentBuilder.BuildTable.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
