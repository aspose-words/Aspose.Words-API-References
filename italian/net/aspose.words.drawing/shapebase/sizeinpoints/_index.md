---
title: ShapeBase.SizeInPoints
linktitle: SizeInPoints
articleTitle: SizeInPoints
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase SizeInPoints per recuperare e gestire facilmente le dimensioni delle forme in punti, per un controllo preciso della progettazione.
type: docs
weight: 540
url: /it/net/aspose.words.drawing/shapebase/sizeinpoints/
---
## ShapeBase.SizeInPoints property

Ottiene la dimensione della forma in punti.

```csharp
public SizeF SizeInPoints { get; }
```

## Esempi

Mostra come verificare le dimensioni di una forma e il linguaggio di markup.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
