---
title: ShapeBase.IsLayoutInCell
linktitle: IsLayoutInCell
articleTitle: IsLayoutInCell
second_title: Aspose.Words för .NET
description: Upptäck egenskapen ShapeBase IsLayoutInCell, styr formars placering i tabeller för ökad designflexibilitet och förbättrad layouthantering.
type: docs
weight: 330
url: /sv/net/aspose.words.drawing/shapebase/islayoutincell/
---
## ShapeBase.IsLayoutInCell property

Hämtar eller anger en flagga som anger om formen visas inuti en tabell eller utanför den.

```csharp
public bool IsLayoutInCell { get; set; }
```

## Anmärkningar

Standardvärdet är`sann`.

Har endast effekt för former på den översta nivån, egenskapen[`WrapType`](../wraptype/) varav är satt till value annat än[`Inline`](../../../aspose.words/inline/).

## Exempel

Visar hur man avgör hur en form ska visas i en tabellcell.

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

// Sätt egenskapen "IsLayoutInCell" till "true" för att visa formen som ett infogat element inuti cellens stycke.
// Koordinatorigo som avgör formens plats kommer att vara det övre vänstra hörnet av formens cell.
// Om vi ändrar storleken på cellen kommer formen att flyttas för att bibehålla samma position med början från cellens övre vänstra hörn.
// Sätt egenskapen "IsLayoutInCell" till "false" för att visa formen som en oberoende flytande form.
// Koordinatorigo som avgör formens plats kommer att vara sidans övre vänstra hörn,
// och formen kommer inte att reagera på någon storleksändring av dess cell.
shape.IsLayoutInCell = isLayoutInCell;

// Vi kan bara tillämpa egenskapen "IsLayoutInCell" på flytande former.
shape.WrapType = WrapType.None;

doc.Save(ArtifactsDir + "Shape.LayoutInTableCell.docx");
```

### Se även

* class [ShapeBase](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
