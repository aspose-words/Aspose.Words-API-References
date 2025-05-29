---
title: ShapeBase.Bounds
linktitle: Bounds
articleTitle: Bounds
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase Bounds per gestire senza sforzo la posizione e le dimensioni della tua forma, migliorando la precisione e l'efficienza della tua progettazione.
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

Ignora il blocco delle proporzioni durante l'impostazione.

Per una forma di livello superiore, il valore è espresso in punti ed è relativo all'ancoraggio della forma.

Per le forme in un gruppo, il valore è espresso nello spazio di coordinate e nelle unità del gruppo padre.

## Esempi

Mostra come verificare i confini dei blocchi contenenti forme.

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

// Crea una forma di gruppo, quindi imposta la dimensione del blocco che la contiene utilizzando la proprietà "Bounds".
GroupShape group = new GroupShape(doc);
group.Bounds = new RectangleF(0, 100, 250, 250);

Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);

// Crea un rettangolo, verifica la dimensione del blocco che lo delimita, quindi aggiungilo alla forma del gruppo.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 700,
    Top = 700
};

Assert.AreEqual(new RectangleF(700, 700, 100, 100), shape.BoundsInPoints);

group.AppendChild(shape);

// Il piano cartesiano della forma del gruppo ha la sua origine nell'angolo in alto a sinistra del blocco contenitore,
// e le coordinate x e y di (1000, 1000) nell'angolo in basso a destra.
// La nostra forma di gruppo ha una dimensione di 250x250 pt, quindi ogni 4 pt sul piano cartesiano della forma di gruppo
// si traduce in 1 pt nel piano cartesiano del corpo del documento.
// Ogni forma che inseriamo si ridurrà di dimensioni di un fattore 4.
// La modifica nella proprietà "BoundsInPoints" della forma rifletterà questo.
Assert.AreEqual(new RectangleF(175, 275, 25, 25), shape.BoundsInPoints);

doc.FirstSection.Body.FirstParagraph.AppendChild(group);

// Inserisce una forma e la posiziona all'esterno dei limiti del blocco contenitore della forma del gruppo.
shape = new Shape(doc, ShapeType.Rectangle)
{
    Width = 100,
    Height = 100,
    Left = 1000,
    Top = 1000
};

group.AppendChild(shape);

// L'ingombro della forma del gruppo nel corpo del documento è aumentato, ma il blocco contenitore rimane lo stesso.
Assert.AreEqual(new RectangleF(0, 100, 250, 250), group.BoundsInPoints);
Assert.AreEqual(new RectangleF(250, 350, 25, 25), shape.BoundsInPoints);

doc.Save(ArtifactsDir + "Shape.Bounds.docx");
```

Mostra come creare e popolare una forma di gruppo.

```csharp
Document doc = new Document();

// Crea una forma di gruppo. Una forma di gruppo può visualizzare una raccolta di nodi di forma figlio.
// In Microsoft Word, facendo clic all'interno del confine della forma del gruppo o su una delle forme figlio della forma del gruppo, verrà
// seleziona tutte le altre forme figlio all'interno di questo gruppo e consentirci di ridimensionare e spostare tutte le forme contemporaneamente.
GroupShape group = new GroupShape(doc);

Assert.AreEqual(WrapType.None, group.WrapType);

// Crea una forma di gruppo da 400 pt x 400 pt e posizionala nell'origine delle coordinate della forma mobile del documento.
group.Bounds = new RectangleF(0, 0, 400, 400);

 // Imposta la dimensione del piano cartesiano interno del gruppo su 500 x 500 pt.
// L'angolo in alto a sinistra del gruppo avrà una coordinata x e y di (0, 0),
// e l'angolo in basso a destra avrà le coordinate x e y di (500, 500).
group.CoordSize = new Size(500, 500);

 // Imposta le coordinate dell'angolo in alto a sinistra del gruppo su (-250, -250).
// Il centro del gruppo avrà ora un valore di coordinata x e y pari a (0, 0),
// e l'angolo in basso a destra sarà a (250, 250).
group.CoordOrigin = new Point(-250, -250);

// Crea un rettangolo che visualizzerà il confine di questa forma di gruppo e aggiungilo al gruppo.
Shape child1 = new Shape(doc, ShapeType.Rectangle)
{
    Width = group.CoordSize.Width,
    Height = group.CoordSize.Height,
    Left = group.CoordOrigin.X,
    Top = group.CoordOrigin.Y
};
group.AppendChild(child1);

// Una volta che una forma fa parte di un gruppo di forme, possiamo accedervi come nodo figlio e quindi modificarla.
((Shape)group.GetChild(NodeType.Shape, 0, true)).Stroke.DashStyle = DashStyle.Dash;

// Crea una piccola stella rossa e inseriscila nel gruppo.
// Allinea la forma con l'origine delle coordinate del gruppo, che abbiamo spostato al centro.
Shape child2 = new Shape(doc, ShapeType.Star)
{
    Width = 20,
    Height = 20,
    Left = -10,
    Top = -10,
    FillColor = Color.Red
};
group.AppendChild(child2);

// Inserisci un rettangolo, quindi inserisci un rettangolo leggermente più piccolo nello stesso posto con un'immagine.
// Le forme più recenti che aggiungiamo al gruppo si sovrappongono a quelle più vecchie. Il rettangolo azzurro si sovrapporrà parzialmente alla stella rossa,
// e quindi la forma con l'immagine si sovrapporrà al rettangolo azzurro, usandolo come cornice.
// Non possiamo usare le proprietà "ZOrder" delle forme per manipolare la loro disposizione all'interno di un gruppo di forme.
Shape child3 = new Shape(doc, ShapeType.Rectangle)
{
    Width = 250,
    Height = 250,
    Left = -250,
    Top = -250,
    FillColor = Color.LightBlue
};
group.AppendChild(child3);

Shape child4 = new Shape(doc, ShapeType.Image)
{
    Width = 200,
    Height = 200,
    Left = -225,
    Top = -225
};
group.AppendChild(child4);

((Shape)group.GetChild(NodeType.Shape, 3, true)).ImageData.SetImage(ImageDir + "Logo.jpg");

// Inserisci una casella di testo nella forma del gruppo. Imposta la proprietà "Sinistra" in modo che il bordo destro della casella di testo
// tocca il limite destro della forma del gruppo. Imposta la proprietà "Top" in modo che la casella di testo si trovi all'esterno.
// il confine della forma del gruppo, con la sua dimensione superiore allineata lungo il margine inferiore della forma del gruppo.
Shape child5 = new Shape(doc, ShapeType.TextBox)
{
    Width = 200,
    Height = 50,
    Left = group.CoordSize.Width + group.CoordOrigin.X - 200,
    Top = group.CoordSize.Height + group.CoordOrigin.Y
};
group.AppendChild(child5);

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
