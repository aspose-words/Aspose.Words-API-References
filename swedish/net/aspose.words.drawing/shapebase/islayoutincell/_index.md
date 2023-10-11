---
title: ShapeBase.IsLayoutInCell
second_title: Aspose.Words för .NET API Referens
description: ShapeBase fast egendom. Hämtar eller sätter en flagga som indikerar om formen visas inuti en tabell eller utanför den.
type: docs
weight: 310
url: /sv/net/aspose.words.drawing/shapebase/islayoutincell/
---
## ShapeBase.IsLayoutInCell property

Hämtar eller sätter en flagga som indikerar om formen visas inuti en tabell eller utanför den.

```csharp
public bool IsLayoutInCell { get; set; }
```

### Anmärkningar

Standardvärdet är`Sann`.

Har effekt endast för toppnivåformer, egenskapen[`WrapType`](../wraptype/) varav är satt till värde annat än[`Inline`](../../../aspose.words/inline/).

### Exempel

Visar hur man bestämmer hur en form ska visas i en tabellcell.

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

// Ställ in egenskapen "IsLayoutInCell" till "true" för att visa formen som ett inline-element inuti cellens stycke.
// Koordinatursprunget som bestämmer formens plats kommer att vara det övre vänstra hörnet av formens cell.
// Om vi ändrar storlek på cellen kommer formen att flyttas för att behålla samma position från cellens övre vänstra hörn.
// Ställ in egenskapen "IsLayoutInCell" till "false" för att visa formen som en oberoende flytande form.
// Koordinatursprunget som bestämmer formens plats kommer att vara det övre vänstra hörnet på sidan,
// och formen kommer inte att svara på om storleken på cellen ändras.
shape.IsLayoutInCell = isLayoutInCell;

// Vi kan bara tillämpa egenskapen "IsLayoutInCell" på flytande former.
shape.WrapType = WrapType.None;

doc.Save(ArtifactsDir + "Shape.LayoutInTableCell.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../shapebase/)
* hopsättning [Aspose.Words](../../../)


