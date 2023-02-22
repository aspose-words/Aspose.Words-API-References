---
title: ShapeBase.HorizontalAlignment
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. Specifica come posizionare la forma orizzontalmente.
type: docs
weight: 210
url: /it/net/aspose.words.drawing/shapebase/horizontalalignment/
---
## ShapeBase.HorizontalAlignment property

Specifica come posizionare la forma orizzontalmente.

```csharp
public HorizontalAlignment HorizontalAlignment { get; set; }
```

### Osservazioni

Il valore predefinito èNone.

Ha effetto solo per le forme mobili di livello superiore.

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

* enum [HorizontalAlignment](../../horizontalalignment/)
* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


