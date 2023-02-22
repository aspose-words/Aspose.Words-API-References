---
title: Fill.GradientStyle
second_title: Aspose.Words per .NET API Reference
description: Fill proprietà. Ottiene lo stile del gradienteGradientStyle per il riempimento.
type: docs
weight: 60
url: /it/net/aspose.words.drawing/fill/gradientstyle/
---
## Fill.GradientStyle property

Ottiene lo stile del gradiente[`GradientStyle`](../../gradientstyle/) per il riempimento.

```csharp
public GradientStyle GradientStyle { get; }
```

### Esempi

Mostra come riempire una forma con una sfumatura.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Applica il riempimento sfumato di un colore alla forma con ForeColor del riempimento sfumato.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Applica un riempimento sfumato a due colori alla forma.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Cambia BackColor del riempimento sfumato.
shape.Fill.BackColor = Color.Yellow;
// Nota che cambia "GradientAngle" per "GradientStyle.FromCorner/GradientStyle.FromCenter"
// il riempimento sfumato non ottiene alcun effetto, funzionerà solo per il gradiente lineare.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Usa l'opzione di conformità per definire la forma usando DML se vuoi ottenere "GradientStyle",
// Proprietà "GradientVariant" e "GradientAngle" dopo il salvataggio del documento.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Guarda anche

* enum [GradientStyle](../../gradientstyle/)
* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../fill/)
* assemblea [Aspose.Words](../../../)


