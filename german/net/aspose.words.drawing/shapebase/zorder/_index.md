---
title: ShapeBase.ZOrder
linktitle: ZOrder
articleTitle: ZOrder
second_title: Aspose.Words für .NET
description: ShapeBase ZOrder eigendom. Bestimmt die Anzeigereihenfolge überlappender Formen in C#.
type: docs
weight: 610
url: /de/net/aspose.words.drawing/shapebase/zorder/
---
## ShapeBase.ZOrder property

Bestimmt die Anzeigereihenfolge überlappender Formen.

```csharp
public int ZOrder { get; set; }
```

## Bemerkungen

Hat nur Auswirkungen auf Formen der obersten Ebene.

Der Standardwert ist 0.

Die Zahl gibt die Stapelpriorität an. Eine Form mit einer höheren Zahl wird angezeigt , als würde sie eine Form mit einer niedrigeren Zahl überlappen (vor ihr).

Die Reihenfolge überlappender Formen ist für Formen in der Kopfzeile und im Haupttext des Dokuments unabhängig.

Die Anzeigereihenfolge untergeordneter Formen in einer Gruppenform wird durch ihre Reihenfolge innerhalb der Gruppenform bestimmt.

## Beispiele

Zeigt, wie die Reihenfolge von Formen manipuliert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie drei verschiedenfarbige Rechtecke ein, die sich teilweise überlappen.
// Wenn wir eine Form einfügen, die eine andere Form überlappt, platziert Aspose.Words die neuere Form über der alten.
// Das hellgrüne Rechteck überlappt das hellblaue Rechteck und verdeckt es teilweise.
// und das hellblaue Rechteck verdeckt das orangefarbene Rechteck.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);
shape.FillColor = Color.Orange;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 150,
    RelativeVerticalPosition.TopMargin, 150, 200, 200, WrapType.None);
shape.FillColor = Color.LightBlue;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 200, 200, WrapType.None);
shape.FillColor = Color.LightGreen;

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

// Die Eigenschaft „ZOrder“ einer Form bestimmt ihre Stapelpriorität unter anderen überlappenden Formen.
// Wenn zwei überlappende Formen unterschiedliche „ZOrder“-Werte haben,
// Microsoft Word platziert die Form mit einem höheren Wert über der Form mit dem niedrigeren Wert. 
// Legen Sie die „ZOrder“-Werte unserer Formen fest, um das erste orangefarbene Rechteck über dem zweiten hellblauen zu platzieren
// und das zweite hellblaue Rechteck über dem dritten hellgrünen Rechteck.
// Dies wird ihre ursprüngliche Stapelreihenfolge umkehren.
shapes[0].ZOrder = 3;
shapes[1].ZOrder = 2;
shapes[2].ZOrder = 1;

doc.Save(ArtifactsDir + "Shape.ZOrder.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
