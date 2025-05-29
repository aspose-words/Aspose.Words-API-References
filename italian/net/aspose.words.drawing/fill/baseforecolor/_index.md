---
title: Fill.BaseForeColor
linktitle: BaseForeColor
articleTitle: BaseForeColor
second_title: Aspose.Words per .NET
description: Scopri la proprietà BaseForeColor per accedere a un oggetto Color che rappresenta il vero colore di primo piano del tuo riempimento, migliorando la chiarezza e l'attrattiva del tuo design.
type: docs
weight: 40
url: /it/net/aspose.words.drawing/fill/baseforecolor/
---
## Fill.BaseForeColor property

Ottiene un oggetto Color che rappresenta il colore di base in primo piano per fill senza modificatori.

```csharp
public Color BaseForeColor { get; }
```

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

* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
