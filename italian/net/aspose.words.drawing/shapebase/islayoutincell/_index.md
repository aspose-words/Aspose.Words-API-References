---
title: ShapeBase.IsLayoutInCell
linktitle: IsLayoutInCell
articleTitle: IsLayoutInCell
second_title: Aspose.Words per .NET
description: Scopri la proprietà IsLayoutInCell di ShapeBase, controlla il posizionamento delle forme nelle tabelle per una maggiore flessibilità di progettazione e una migliore gestione del layout.
type: docs
weight: 330
url: /it/net/aspose.words.drawing/shapebase/islayoutincell/
---
## ShapeBase.IsLayoutInCell property

Ottiene o imposta un flag che indica se la forma viene visualizzata all'interno di una tabella o all'esterno di essa.

```csharp
public bool IsLayoutInCell { get; set; }
```

## Osservazioni

Il valore predefinito è`VERO`.

Ha effetto solo per le forme di livello superiore, la proprietà[`WrapType`](../wraptype/) di cui è impostato su value diverso da[`Inline`](../../../aspose.words/inline/).

## Esempi

Mostra come stabilire come visualizzare una forma in una cella di una tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.InsertCell();
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.BottomPadding = 20;
tableStyle.LeftPadding = 10;
tableStyle.RightPadding = 10;
tableStyle.TopPadding = 20;
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Single;

table.Style = tableStyle;

builder.MoveTo(table.FirstRow.FirstCell.FirstParagraph);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 100, 100, 100, WrapType.None);

// Impostare la proprietà "IsLayoutInCell" su "true" per visualizzare la forma come elemento in linea all'interno del paragrafo della cella.
// L'origine delle coordinate che determinerà la posizione della forma sarà l'angolo in alto a sinistra della cella della forma.
// Se ridimensioniamo la cella, la forma si sposterà per mantenere la stessa posizione a partire dall'angolo in alto a sinistra della cella.
// Impostare la proprietà "IsLayoutInCell" su "false" per visualizzare la forma come forma mobile indipendente.
// L'origine delle coordinate che determinerà la posizione della forma sarà l'angolo in alto a sinistra della pagina,
// e la forma non risponderà ad alcun ridimensionamento della sua cella.
shape.IsLayoutInCell = isLayoutInCell;

// Possiamo applicare la proprietà "IsLayoutInCell" solo alle forme mobili.
shape.WrapType = WrapType.None;

doc.Save(ArtifactsDir + "Shape.LayoutInTableCell.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
