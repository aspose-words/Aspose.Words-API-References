---
title: DocumentBuilder.CurrentSection
second_title: Aspose.Words per .NET API Reference
description: DocumentBuilder proprietà. Ottiene la sezione attualmente selezionata in questo DocumentBuilder.
type: docs
weight: 60
url: /it/net/aspose.words/documentbuilder/currentsection/
---
## DocumentBuilder.CurrentSection property

Ottiene la sezione attualmente selezionata in questo DocumentBuilder.

```csharp
public Section CurrentSection { get; }
```

### Esempi

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

// Usa la proprietà "RelativeVerticalPosition" in modo simile per posizionare la forma 80pt sotto la parte superiore della pagina.
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

* class [Section](../../section/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../documentbuilder/)
* assemblea [Aspose.Words](../../../)


