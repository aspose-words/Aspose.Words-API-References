---
title: ShapeBase.Bottom
linktitle: Bottom
articleTitle: Bottom
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase Bottom per accedere facilmente alla posizione del bordo inferiore del blocco contenitore della tua forma, per un controllo preciso del design.
type: docs
weight: 60
url: /it/net/aspose.words.drawing/shapebase/bottom/
---
## ShapeBase.Bottom property

Ottiene la posizione del bordo inferiore del blocco contenitore della forma.

```csharp
public double Bottom { get; }
```

## Osservazioni

Per una forma di livello superiore, il valore è espresso in punti ed è relativo all'ancoraggio della forma.

Per le forme in un gruppo, il valore è espresso nello spazio di coordinate e nelle unità del gruppo padre.

## Esempi

Mostra come inserire un'immagine mobile e specificarne la posizione e le dimensioni.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Configura la proprietà "RelativeHorizontalPosition" della forma per trattare il valore della proprietà "Left"
 // come distanza orizzontale della forma, in punti, dal lato sinistro della pagina.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Imposta la distanza orizzontale della forma dal lato sinistro della pagina su 100.
shape.Left = 100;

// Utilizzare la proprietà "RelativeVerticalPosition" in modo simile per posizionare la forma 80 pt sotto la parte superiore della pagina.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Imposta l'altezza della forma, che ridimensionerà automaticamente la larghezza per preservare le dimensioni.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Le proprietà "Bottom" e "Right" contengono i bordi inferiore e destro dell'immagine.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
