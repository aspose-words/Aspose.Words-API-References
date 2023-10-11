---
title: ImageData.GrayScale
second_title: Aspose.Words per .NET API Reference
description: ImageData proprietà. Determina se unimmagine verrà visualizzata in modalità scala di grigi.
type: docs
weight: 100
url: /it/net/aspose.words.drawing/imagedata/grayscale/
---
## ImageData.GrayScale property

Determina se un'immagine verrà visualizzata in modalità scala di grigi.

```csharp
public bool GrayScale { get; set; }
```

### Osservazioni

Il valore predefinito è`falso`.

### Esempi

Mostra come modificare i dati dell'immagine di una forma.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// Importa una forma dal documento di origine e la aggiunge al primo paragrafo.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// La forma importata contiene un'immagine. Possiamo accedere alle proprietà dell'immagine e ai dati grezzi tramite l'oggetto ImageData.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// Se un'immagine non ha bordi, il suo oggetto ImageData definirà il colore del bordo come vuoto.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// Questa immagine non si collega a un'altra forma o file immagine nel file system locale.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// Le proprietà "Luminosità" e "Contrasto" definiscono la luminosità e il contrasto dell'immagine
// su una scala 0-1, con il valore predefinito pari a 0,5.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// I valori di luminosità e contrasto sopra indicati hanno creato un'immagine con molto bianco.
// Possiamo selezionare un colore con la proprietà ChromaKey da sostituire con la trasparenza, come il bianco.
imageData.ChromaKey = Color.White;

// Importa nuovamente la forma sorgente e imposta l'immagine su monocromatica.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// Importa nuovamente la forma sorgente per creare una terza immagine e impostarla su BiLevel.
// BiLevel imposta ogni pixel su nero o bianco, a seconda di quale sia il colore più vicino all'originale.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// Il ritaglio è determinato su una scala 0-1. Ritagliare un lato di 0,3
// ritaglierà il 30% dell'immagine sul lato ritagliato.
importedShape.ImageData.CropBottom = 0.3;
importedShape.ImageData.CropLeft = 0.3;
importedShape.ImageData.CropTop = 0.3;
importedShape.ImageData.CropRight = 0.3;

dstDoc.Save(ArtifactsDir + "Drawing.ImageData.docx");
```

### Guarda anche

* class [ImageData](../)
* spazio dei nomi [Aspose.Words.Drawing](../../imagedata/)
* assemblea [Aspose.Words](../../../)


