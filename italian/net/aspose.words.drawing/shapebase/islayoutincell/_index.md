---
title: ShapeBase.IsLayoutInCell
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. Ottiene o imposta un flag che indica se la forma viene visualizzata allinterno o allesterno di una tabella.
type: docs
weight: 310
url: /it/net/aspose.words.drawing/shapebase/islayoutincell/
---
## ShapeBase.IsLayoutInCell property

Ottiene o imposta un flag che indica se la forma viene visualizzata all'interno o all'esterno di una tabella.

```csharp
public bool IsLayoutInCell { get; set; }
```

### Osservazioni

Il valore predefinito è`VERO`.

Ha effetto solo per le forme di livello superiore, la proprietà[`WrapType`](../wraptype/) di cui è impostato su value diverso da[`Inline`](../../../aspose.words/inline/).

### Esempi

Mostra come determinare come visualizzare una forma in una cella di tabella.

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

// Imposta la proprietà "IsLayoutInCell" su "true" per visualizzare la forma come elemento in linea all'interno del paragrafo della cella.
// L'origine delle coordinate che determinerà la posizione della forma sarà l'angolo in alto a sinistra della cella della forma.
// Se ridimensioniamo la cella, la forma si sposterà per mantenere la stessa posizione partendo dall'angolo in alto a sinistra della cella.
// Imposta la proprietà "IsLayoutInCell" su "false" per visualizzare la forma come forma mobile indipendente.
// L'origine delle coordinate che determinerà la posizione della forma sarà l'angolo in alto a sinistra della pagina,
// e la forma non risponderà ad alcun ridimensionamento della sua cella.
shape.IsLayoutInCell = isLayoutInCell;

// Possiamo applicare la proprietà "IsLayoutInCell" solo alle forme fluttuanti.
shape.WrapType = WrapType.None;

doc.Save(ArtifactsDir + "Shape.LayoutInTableCell.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


