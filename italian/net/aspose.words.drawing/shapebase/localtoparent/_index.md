---
title: ShapeBase.LocalToParent
linktitle: LocalToParent
articleTitle: LocalToParent
second_title: Aspose.Words per .NET
description: Trasforma le coordinate locali nello spazio della forma padre con il metodo ShapeBase LocalToParent. Aumenta la precisione dei tuoi progetti di modellazione 3D oggi stesso!
type: docs
weight: 680
url: /it/net/aspose.words.drawing/shapebase/localtoparent/
---
## ShapeBase.LocalToParent method

Converte un valore dallo spazio delle coordinate locali nello spazio delle coordinate della forma padre.

```csharp
public PointF LocalToParent(PointF value)
```

## Esempi

Mostra come tradurre la posizione delle coordinate x e y sul piano cartesiano di una forma in una posizione sul piano cartesiano della forma padre.

```csharp
Document doc = new Document();

// Inserisci una forma di gruppo e posizionala 100 punti sotto e a destra di
// punto di origine delle coordinate x e Y del documento.
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(100, 100, 500, 500);

// Utilizzare il metodo "LocalToParent" per determinare che (0, 0) sulle coordinate x e y interne del gruppo
// si trova sul sistema di coordinate (100, 100) della sua forma padre. La forma padre del gruppo è il documento stesso.
Assert.AreEqual(new PointF(100, 100), group.LocalToParent(new PointF(0, 0)));

// Per impostazione predefinita, il piano cartesiano interno di una forma ha l'angolo in alto a sinistra in (0, 0),
// e l'angolo in basso a destra a (1000, 1000). Grazie alle sue dimensioni, la forma del nostro gruppo copre un'area di 500 pt x 500 pt.
// nel piano del documento. Ciò significa che uno spostamento di 1 pt sul piano cartesiano del documento si tradurrà
// a uno spostamento di 2 punti sul piano cartesiano della forma del gruppo.
Assert.AreEqual(new PointF(150, 150), group.LocalToParent(new PointF(100, 100)));
Assert.AreEqual(new PointF(200, 200), group.LocalToParent(new PointF(200, 200)));
Assert.AreEqual(new PointF(250, 250), group.LocalToParent(new PointF(300, 300)));

// Sposta l'origine degli assi x e y della forma del gruppo dall'angolo in alto a sinistra al centro.
// In questo modo le coordinate interne del gruppo verranno ulteriormente spostate rispetto alle coordinate del documento.
group.CoordOrigin = new Point(-250, -250);

Assert.AreEqual(new PointF(375, 375), group.LocalToParent(new PointF(300, 300)));

// La modifica della scala del piano cartesiano inciderà anche sulle posizioni relative.
group.CoordSize = new Size(500, 500);

Assert.AreEqual(new PointF(650, 650), group.LocalToParent(new PointF(300, 300)));

// Se desideriamo aggiungere una forma a questo gruppo definendone la posizione in base a una posizione nel documento,
// Per prima cosa dovremo confermare una posizione nella forma del gruppo che corrisponda alla posizione del documento.
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
