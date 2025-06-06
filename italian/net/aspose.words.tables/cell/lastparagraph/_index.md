---
title: Cell.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words per .NET
description: Scopri la proprietà Cell LastParagraph. Accedi facilmente all'ultimo paragrafo dagli elementi figlio immediati per una gestione efficiente dei contenuti.
type: docs
weight: 60
url: /it/net/aspose.words.tables/cell/lastparagraph/
---
## Cell.LastParagraph property

Ottiene l'ultimo paragrafo tra i figli immediati.

```csharp
public Paragraph LastParagraph { get; }
```

## Esempi

Mostra come applicare le impostazioni ai bordi verticali nel formato di una riga di una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea una tabella con bordi interni rossi e blu.
Table table = builder.StartTable();

for (int i = 0; i < 3; i++)
{
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 1");
    builder.InsertCell();
    builder.Write($"Row {i + 1}, Column 2");

    Row row = builder.EndRow();
    BorderCollection borders = row.RowFormat.Borders;

    // Regola l'aspetto dei bordi che appariranno tra le righe.
    borders.Horizontal.Color = Color.Red;
    borders.Horizontal.LineStyle = LineStyle.Dot;
    borders.Horizontal.LineWidth = 2.0d;

    // Regola l'aspetto dei bordi che appariranno tra le celle.
    borders.Vertical.Color = Color.Blue;
    borders.Vertical.LineStyle = LineStyle.Dot;
    borders.Vertical.LineWidth = 2.0d;
}

// Un formato di riga e il paragrafo interno di una cella utilizzano impostazioni di bordo diverse.
Border border = table.FirstRow.FirstCell.LastParagraph.ParagraphFormat.Borders.Vertical;

Assert.AreEqual(Color.Empty.ToArgb(), border.Color.ToArgb());
Assert.AreEqual(0.0d, border.LineWidth);
Assert.AreEqual(LineStyle.None, border.LineStyle);

doc.Save(ArtifactsDir + "Border.VerticalBorders.docx");
```

### Guarda anche

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Cell](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
