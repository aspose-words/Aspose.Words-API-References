---
title: GradientStyle Enum
linktitle: GradientStyle
articleTitle: GradientStyle
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.GradientStyle per stili di riempimento sfumato personalizzabili, che arricchiscono i design dei tuoi documenti con elementi visivi vivaci.
type: docs
weight: 1330
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
| None | `-1` | Nessun gradiente. |
| Horizontal | `1` | Gradiente che corre orizzontalmente su un oggetto. |
| Vertical | `2` | Gradiente che corre verticalmente lungo un oggetto. |
| DiagonalUp | `3` | Gradiente diagonale che si sposta da un angolo inferiore all'angolo opposto. |
| DiagonalDown | `4` | Gradiente diagonale che si sposta da un angolo superiore verso l'angolo opposto. |
| FromCorner | `5` | Gradiente che va da un angolo agli altri tre angoli. |
| FromCenter | `6` | Gradiente che va dal centro verso gli angoli. |

## Esempi

Mostra come riempire una forma con sfumature.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Applica un riempimento sfumato a un colore alla forma con ForeColor del riempimento sfumato.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Applica un riempimento sfumato a due colori alla forma.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Cambia il colore di sfondo del riempimento sfumato.
shape.Fill.BackColor = Color.Yellow;
// Nota che cambia "GradientAngle" per "GradientStyle.FromCorner/GradientStyle.FromCenter"
// il riempimento sfumato non ha alcun effetto, funzionerà solo con gradienti lineari.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Utilizzare l'opzione di conformità per definire la forma utilizzando DML se si desidera ottenere "GradientStyle",
// Proprietà "GradientVariant" e "GradientAngle" dopo il salvataggio del documento.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
