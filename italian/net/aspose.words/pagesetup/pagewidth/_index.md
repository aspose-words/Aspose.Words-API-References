---
title: PageSetup.PageWidth
linktitle: PageWidth
articleTitle: PageWidth
second_title: Aspose.Words per .NET
description: PageSetup PageWidth proprietà. Restituisce o imposta la larghezza della pagina in punti in C#.
type: docs
weight: 340
url: /it/net/aspose.words/pagesetup/pagewidth/
---
## PageSetup.PageWidth property

Restituisce o imposta la larghezza della pagina in punti.

```csharp
public double PageWidth { get; set; }
```

## Esempi

Mostra come inserire un'immagine e utilizzarla come filigrana.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci l'immagine nell'intestazione in modo che sia visibile su ogni pagina.
Image image = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(image);
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Posiziona l'immagine al centro della pagina.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

Mostra come inserire un'immagine e utilizzarla come filigrana (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci l'immagine nell'intestazione in modo che sia visibile su ogni pagina.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

using (SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png"))
{
    builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
    Shape shape = builder.InsertImage(image);
    shape.WrapType = WrapType.None;
    shape.BehindText = true;

    // Posiziona l'immagine al centro della pagina.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
    shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
    shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
    shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermarkNetStandard2.docx");
```

Mostra come inserire un'immagine mobile e specificarne la posizione e le dimensioni.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Configura la proprietà "RelativeHorizontalPosition" della forma per trattare il valore della proprietà "Left"
 // come la distanza orizzontale della forma, in punti, dal lato sinistro della pagina.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Imposta la distanza orizzontale della forma dal lato sinistro della pagina su 100.
shape.Left = 100;

// Utilizza la proprietà "RelativeVerticalPosition" in modo simile per posizionare la forma 80pt sotto la parte superiore della pagina.
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

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
