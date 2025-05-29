---
title: Stroke.BaseForeColor
linktitle: BaseForeColor
articleTitle: BaseForeColor
second_title: Aspose.Words per .NET
description: Scopri la proprietà Stroke BaseForeColor per accedere facilmente al colore di base non modificato del tuo tratto, per un controllo preciso del design.
type: docs
weight: 40
url: /it/net/aspose.words.drawing/stroke/baseforecolor/
---
## Stroke.BaseForeColor property

Ottiene il colore di base del primo piano del tratto senza modificatori.

```csharp
public Color BaseForeColor { get; }
```

## Osservazioni

Il valore predefinito per un[`Shape`](../../shape/) è Black .

## Esempi

Mostra come ottenere il colore di primo piano senza modificatori.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
shape.Fill.ForeColor = Color.Red;
shape.Fill.ForeTintAndShade = 0.5;
shape.Stroke.Fill.ForeColor = Color.Green;
shape.Stroke.Fill.Transparency = 0.5;

Assert.AreEqual(Color.FromArgb(255, 255, 188, 188).ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.BaseForeColor.ToArgb());

Assert.AreEqual(Color.FromArgb(128, 0, 128, 0).ToArgb(), shape.Stroke.ForeColor.ToArgb());
Assert.AreEqual(Color.Green.ToArgb(), shape.Stroke.BaseForeColor.ToArgb());

Assert.AreEqual(Color.Green.ToArgb(), shape.Stroke.Fill.ForeColor.ToArgb());
Assert.AreEqual(Color.Green.ToArgb(), shape.Stroke.Fill.BaseForeColor.ToArgb());
```

### Guarda anche

* class [Stroke](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
