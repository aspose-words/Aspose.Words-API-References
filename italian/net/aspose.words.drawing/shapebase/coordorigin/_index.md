---
title: ShapeBase.CoordOrigin
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. Le coordinate nellangolo in alto a sinistra del blocco contenitore di questa forma.
type: docs
weight: 110
url: /it/net/aspose.words.drawing/shapebase/coordorigin/
---
## ShapeBase.CoordOrigin property

Le coordinate nell'angolo in alto a sinistra del blocco contenitore di questa forma.

```csharp
public Point CoordOrigin { get; set; }
```

### Osservazioni

Il valore predefinito è (0,0).

### Esempi

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

Mostra come creare e popolare una forma di gruppo.

```csharp
Document doc = new Document();

// Crea una forma di gruppo. Una forma di gruppo può visualizzare una raccolta di nodi di forme figlio.
// In Microsoft Word, facendo clic all'interno del limite della forma del gruppo o su una delle forme secondarie della forma del gruppo verrà eseguito
// seleziona tutte le altre forme figlie all'interno di questo gruppo e ci consente di ridimensionare e spostare tutte le forme contemporaneamente.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// Crea una forma di gruppo da 400 pt x 400 pt e posizionala nell'origine delle coordinate della forma mobile del documento.
group.Bounds = new RectangleF(0, 0, 400, 400);

// Imposta la dimensione del piano delle coordinate interne del gruppo su 500 x 500 pt. 
// L'angolo in alto a sinistra del gruppo avrà le coordinate xey pari a (0, 0),
// e l'angolo in basso a destra avrà le coordinate xey di (500, 500).
group.CoordSize = new Size(500, 500);

// Imposta le coordinate dell'angolo in alto a sinistra del gruppo su (-250, -250). 
// Il centro del gruppo ora avrà un valore di coordinate xey pari a (0, 0),
// e l'angolo in basso a destra sarà in (250, 250).
group.CoordOrigin = new Point(-250, -250);

// Crea un rettangolo che visualizzerà il confine di questa forma di gruppo e lo aggiungerà al gruppo.
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
});

// Una volta che una forma fa parte di una forma di gruppo, possiamo accedervi come nodo figlio e quindi modificarla.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Crea una piccola stella rossa e inseriscila nel gruppo.
// Allinea la forma con l'origine delle coordinate del gruppo, che abbiamo spostato al centro.
group.AppendChild(new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
});

// Inserisci un rettangolo, quindi inserisci un rettangolo leggermente più piccolo nello stesso punto con un'immagine. 
// Le forme più recenti aggiunte al gruppo si sovrappongono alle forme più vecchie. Il rettangolo azzurro si sovrapporrà parzialmente alla stella rossa,
// e poi la forma con l'immagine si sovrapporrà al rettangolo azzurro, utilizzandolo come cornice.
// Non possiamo usare le proprietà "ZOrder" delle forme per manipolare la loro disposizione all'interno di una forma di gruppo. 
group.AppendChild(new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
});

group.AppendChild(new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
});

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// Inserisci una casella di testo nella forma del gruppo. Imposta la proprietà "Left" in modo che il bordo destro della casella di testo
// tocca il confine destro della forma del gruppo. Imposta la proprietà "Top" in modo che la casella di testo si trovi all'esterno
// il confine della forma del gruppo, con la dimensione superiore allineata lungo il margine inferiore della forma del gruppo.
group.AppendChild(new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
});

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(group);
builder.MoveTo(((Shape)group.GetChild(NodeType.Shape, 4, true)).AppendChild(new Paragraph(doc)));
builder.Write("Hello world!");

doc.Save(ArtifactsDir + "Shape.GroupShape.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


