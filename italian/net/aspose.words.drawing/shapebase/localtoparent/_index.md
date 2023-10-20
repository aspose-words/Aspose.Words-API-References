---
title: ShapeBase.LocalToParent
linktitle: LocalToParent
articleTitle: LocalToParent
second_title: Aspose.Words per .NET
description: ShapeBase LocalToParent metodo. Converte un valore dallo spazio delle coordinate locali nello spazio delle coordinate della forma genitore in C#.
type: docs
weight: 670
url: /it/net/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase.LocalToParent method

Converte un valore dallo spazio delle coordinate locali nello spazio delle coordinate della forma genitore.

```csharp
public PointF LocalToParent(PointF value)
```

## Esempi

Mostra come tradurre la posizione delle coordinate xey sul piano delle coordinate di una forma in una posizione sul piano delle coordinate della forma padre.

```csharp
Document doc = new Document();

// Inserisci una forma di gruppo e posizionala 100 punti sotto e a destra di
// il punto di origine delle coordinate x e Y del documento.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Utilizza il metodo "LocalToParent" per determinare che (0, 0) sulle coordinate x e y interne del gruppo
// si trova su (100, 100) del sistema di coordinate della sua forma principale. Il genitore della forma del gruppo è il documento stesso.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// Per impostazione predefinita, il piano delle coordinate interne di una forma ha l'angolo in alto a sinistra su (0, 0),
// e l'angolo in basso a destra in (1000, 1000). A causa delle sue dimensioni, la forma del nostro gruppo copre un'area di 500 x 500 pt
// nel piano del documento. Ciò significa che verrà traslato un movimento di 1pt sul piano delle coordinate del documento
// a un movimento di 2 punti sul piano delle coordinate della forma del gruppo.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Sposta l'origine degli assi xey della forma del gruppo dall'angolo in alto a sinistra al centro.
// Ciò compenserà ulteriormente le coordinate interne del gruppo rispetto alle coordinate del documento.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// La modifica della scala del piano delle coordinate influenzerà anche le posizioni relative.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Se desideriamo aggiungere una forma a questo gruppo definendone la posizione in base a una posizione nel documento,
// dovremo prima confermare una posizione nella forma del gruppo che corrisponda alla posizione del documento.
Assert.AreEqual(new PointF(700, 700), group.LocalToParent(new PointF(350, 350)));

Shape shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

group.AppendChild(shape);
doc.FirstSection.Body.FirstParagraph.AppendChild(group);

doc.Save(ArtifactsDir + "Shape.LocalToParent.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
