---
title: ShapeBase.BehindText
linktitle: BehindText
articleTitle: BehindText
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase BehindText per controllare la disposizione delle forme nei tuoi progetti, migliorando senza sforzo la visibilità del testo e la precisione del layout.
type: docs
weight: 50
url: /it/net/aspose.words.drawing/shapebase/behindtext/
---
## ShapeBase.BehindText property

Specifica se la forma si trova sotto o sopra il testo.

```csharp
public bool BehindText { get; set; }
```

## Osservazioni

Ha effetto solo sulle forme di livello superiore.

Il valore predefinito è`falso`.

## Esempi

Mostra come inserire un'immagine mobile al centro di una pagina.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un'immagine mobile che apparirà dietro il testo sovrapposto e allineala al centro della pagina.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
