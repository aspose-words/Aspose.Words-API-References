---
title: ShapeBase.IsLayoutInCell
linktitle: IsLayoutInCell
articleTitle: IsLayoutInCell
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase-Eigenschaft „IsLayoutInCell“, steuern Sie die Platzierung von Formen in Tabellen für mehr Designflexibilität und verbessertes Layoutmanagement.
type: docs
weight: 330
url: /de/net/aspose.words.drawing/shapebase/islayoutincell/
---
## ShapeBase.IsLayoutInCell property

Ruft ein Flag ab oder legt es fest, das angibt, ob die Form innerhalb oder außerhalb einer Tabelle angezeigt wird.

```csharp
public bool IsLayoutInCell { get; set; }
```

## Bemerkungen

Der Standardwert ist`WAHR`.

Wirkt sich nur auf Formen der obersten Ebene aus. Die Eigenschaft[`WrapType`](../wraptype/) davon ist auf value gesetzt, anders als[`Inline`](../../../aspose.words/inline/).

## Beispiele

Zeigt, wie Sie bestimmen, wie eine Form in einer Tabellenzelle angezeigt wird.

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

// Setzen Sie die Eigenschaft „IsLayoutInCell“ auf „true“, um die Form als Inline-Element innerhalb des Absatzes der Zelle anzuzeigen.
// Der Koordinatenursprung, der die Position der Form bestimmt, ist die obere linke Ecke der Zelle der Form.
// Wenn wir die Größe der Zelle ändern, wird die Form verschoben, um die gleiche Position beizubehalten, beginnend oben links in der Zelle.
// Setzen Sie die Eigenschaft „IsLayoutInCell“ auf „false“, um die Form als unabhängige schwebende Form anzuzeigen.
// Der Koordinatenursprung, der die Position der Form bestimmt, ist die obere linke Ecke der Seite.
// und die Form reagiert nicht auf eine Größenänderung ihrer Zelle.
shape.IsLayoutInCell = isLayoutInCell;

// Wir können die Eigenschaft „IsLayoutInCell“ nur auf schwebende Formen anwenden.
shape.WrapType = WrapType.None;

doc.Save(ArtifactsDir + "Shape.LayoutInTableCell.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
