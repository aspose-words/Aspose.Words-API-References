---
title: ShapeBase.Bounds
linktitle: Bounds
articleTitle: Bounds
second_title: Aspose.Words per .NET
description: ShapeBase Bounds proprietà. Ottiene o imposta la posizione e la dimensione del blocco contenitore della forma in C#.
type: docs
weight: 70
url: /it/net/aspose.words.drawing/shapebase/bounds/
---
## ShapeBase.Bounds property

Ottiene o imposta la posizione e la dimensione del blocco contenitore della forma.

```csharp
public RectangleF Bounds { get; set; }
```

## Osservazioni

Ignora il blocco delle proporzioni al momento dell'impostazione.

Per una forma di livello superiore, il valore è espresso in punti e relativo all'ancoraggio della forma.

Per le forme in un gruppo, il valore è nello spazio delle coordinate e nelle unità del gruppo principale.

## Esempi

Mostra come verificare la forma contenente i limiti del blocco.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Line, RelativeHorizontalPosition.LeftMargin, 50,
    RelativeVerticalPosition.TopMargin, 50, 100, 100, WrapType.None);
shape.StrokeColor = Color.Orange;

// Anche se la riga stessa occupa poco spazio sulla pagina del documento,
// occupa un blocco contenitore rettangolare, la cui dimensione possiamo determinare utilizzando le proprietà "Bounds".
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.Bounds);
Assert.AreEqual(new RectangleF(50, 50, 100, 100), shape.BoundsInPoints);

// Crea una forma di gruppo, quindi imposta la dimensione del blocco che lo contiene utilizzando la proprietà "Bounds".
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Crea un rettangolo, verifica la dimensione del blocco di delimitazione, quindi aggiungilo alla forma del gruppo.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// Il piano delle coordinate della forma del gruppo ha la sua origine nell'angolo in alto a sinistra del blocco che lo contiene,
// e le coordinate xey di (1000, 1000) nell'angolo in basso a destra.
// La forma del nostro gruppo ha una dimensione di 250x250 pt, quindi ogni 4 punti sul piano delle coordinate della forma del gruppo
// si traduce in 1pt nel piano delle coordinate del corpo del documento.
// Ogni forma che inseriamo si ridurrà anche di dimensioni di un fattore 4.
// La modifica nella proprietà "BoundsInPoints" della forma rifletterà questo.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Inserisci una forma e posizionala all'esterno dei limiti del blocco contenitore della forma del gruppo.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// L'impronta della forma del gruppo nel corpo del documento è aumentata, ma il blocco contenitore rimane lo stesso.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
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
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
