---
title: ShapeBase.CanHaveImage
linktitle: CanHaveImage
articleTitle: CanHaveImage
second_title: Aspose.Words per .NET
description: ShapeBase CanHaveImage proprietà. RestituisceVERO se il tipo di forma consente alla forma di avere unimmagine in C#.
type: docs
weight: 100
url: /it/net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

Restituisce`VERO` se il tipo di forma consente alla forma di avere un'immagine.

```csharp
public bool CanHaveImage { get; }
```

## Osservazioni

Sebbene Microsoft Word abbia un tipo di forma speciale per le immagini, sembra che nei documenti di Microsoft Word qualsiasi forma tranne una forma di gruppo possa avere un'immagine, quindi questa proprietà restituisce`VERO` per tutte le forme tranne[`GroupShape`](../../groupshape/).

## Esempi

Mostra come inserire e ruotare un'immagine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci una forma con un'immagine.
Shape shape = builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Ruota l'immagine di 45 gradi in senso orario.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
