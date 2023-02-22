---
title: ShapeBase.CanHaveImage
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. Restituisce true se il tipo di forma consente alla forma di avere unimmagine.
type: docs
weight: 100
url: /it/net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

Restituisce true se il tipo di forma consente alla forma di avere un'immagine.

```csharp
public bool CanHaveImage { get; }
```

### Osservazioni

Sebbene Microsoft Word abbia un tipo di forma speciale per le immagini, sembra che nei documenti di Microsoft Word qualsiasi forma eccetto una forma di gruppo possa avere un'immagine, quindi questa proprietà restituisce true per tutte le forme tranne[`GroupShape`](../../groupshape/).

### Esempi

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
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


