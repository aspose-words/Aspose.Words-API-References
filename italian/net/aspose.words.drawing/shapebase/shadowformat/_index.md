---
title: ShapeBase.ShadowFormat
linktitle: ShadowFormat
articleTitle: ShadowFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase ShadowFormat per migliorare i tuoi progetti con effetti ombra personalizzabili per le forme. Migliora il tuo appeal visivo oggi stesso!
type: docs
weight: 520
url: /it/net/aspose.words.drawing/shapebase/shadowformat/
---
## ShapeBase.ShadowFormat property

Ottiene la formattazione dell'ombra per la forma.

```csharp
public ShadowFormat ShadowFormat { get; }
```

## Esempi

Mostra come ottenere il colore dell'ombra.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ShadowFormat shadowFormat = shape.ShadowFormat;

Assert.AreEqual(Color.Red.ToArgb(), shadowFormat.Color.ToArgb());
Assert.AreEqual(ShadowType.ShadowMixed, shadowFormat.Type);
```

### Guarda anche

* class [ShadowFormat](../../shadowformat/)
* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
