---
title: Enum GradientStyle
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.GradientStyle enum. Specifica lo stile per un riempimento sfumato.
type: docs
weight: 1000
url: /it/net/aspose.words.drawing/gradientstyle/
---
## GradientStyle enumeration

Specifica lo stile per un riempimento sfumato.

```csharp
public enum GradientStyle
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `-1` | Nessuna sfumatura. |
| Horizontal | `1` | Gradiente che corre orizzontalmente su un oggetto. |
| Vertical | `2` | Gradiente che corre verticalmente lungo un oggetto. |
| DiagonalUp | `3` | Gradiente diagonale che si sposta da un angolo inferiore fino all'angolo opposto. |
| DiagonalDown | `4` | Gradiente diagonale che si sposta da un angolo superiore verso l'angolo opposto. |
| FromCorner | `5` | Gradiente che va da un angolo agli altri tre angoli. |
| FromCenter | `6` | Gradiente che va dal centro verso gli angoli. |

### Esempi

Mostra come riempire una forma con sfumature.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Applica il riempimento sfumato monocolore alla forma con ForeColor del riempimento sfumato.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Applica il riempimento sfumato a due colori alla forma.
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

// Utilizza l'opzione di conformità per definire la forma utilizzando DML se desideri ottenere "GradientStyle",
// Proprietà "GradientVariant" e "GradientAngle" dopo il salvataggio del documento.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)


