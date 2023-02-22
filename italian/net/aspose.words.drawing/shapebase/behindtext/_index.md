---
title: ShapeBase.BehindText
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. Specifica se la forma è al di sotto o al di sopra del testo.
type: docs
weight: 50
url: /it/net/aspose.words.drawing/shapebase/behindtext/
---
## ShapeBase.BehindText property

Specifica se la forma è al di sotto o al di sopra del testo.

```csharp
public bool BehindText { get; set; }
```

### Osservazioni

Ha effetto solo per le forme di livello superiore.

Il valore predefinito è **falso**.

### Esempi

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
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


