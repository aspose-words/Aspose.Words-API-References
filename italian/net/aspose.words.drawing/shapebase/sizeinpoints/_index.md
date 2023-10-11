---
title: ShapeBase.SizeInPoints
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. Ottiene la dimensione della forma in punti.
type: docs
weight: 510
url: /it/net/aspose.words.drawing/shapebase/sizeinpoints/
---
## ShapeBase.SizeInPoints property

Ottiene la dimensione della forma in punti.

```csharp
public SizeF SizeInPoints { get; }
```

### Esempi

Mostra come verificare le dimensioni e il linguaggio di markup di una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


