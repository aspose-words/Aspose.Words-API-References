---
title: BorderCollection.Horizontal
linktitle: Horizontal
articleTitle: Horizontal
second_title: Aspose.Words per .NET
description: Scopri la proprietà BorderCollection Horizontal per bordi di celle e paragrafi senza soluzione di continuità. Migliora il tuo layout con allineamento e stile perfetti!
type: docs
weight: 50
url: /it/net/aspose.words/bordercollection/horizontal/
---
## BorderCollection.Horizontal property

Ottiene il bordo orizzontale utilizzato tra celle o paragrafi conformi.

```csharp
public Border Horizontal { get; }
```

## Esempi

Mostra come applicare le impostazioni ai bordi orizzontali nel formato di un paragrafo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un bordo orizzontale rosso per il paragrafo. Tutti i paragrafi creati in seguito erediteranno queste impostazioni del bordo.
BorderCollection borders = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Borders;
borders.Horizontal.Color = Color.Red;
borders.Horizontal.LineStyle = LineStyle.DashSmallGap;
borders.Horizontal.LineWidth = 3;

// Scrive il testo nel documento senza creare un nuovo paragrafo in seguito.
// Poiché non c'è alcun paragrafo sottostante, il bordo orizzontale non sarà visibile.
builder.Write("Paragraph above horizontal border.");

// Una volta aggiunto un secondo paragrafo, il bordo del primo paragrafo diventerà visibile.
builder.InsertParagraph();
builder.Write("Paragraph below horizontal border.");

doc.Save(ArtifactsDir + "Border.HorizontalBorders.docx");
```

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

* class [Border](../../border/)
* class [BorderCollection](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
