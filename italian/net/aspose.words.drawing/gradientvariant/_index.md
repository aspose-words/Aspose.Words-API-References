---
title: GradientVariant Enum
linktitle: GradientVariant
articleTitle: GradientVariant
second_title: Aspose.Words per .NET
description: Scopri l'enumerazione Aspose.Words.Drawing.GradientVariant per riempimenti sfumati personalizzabili, che arricchiscono i design dei tuoi documenti con stili vivaci.
type: docs
weight: 1340
url: /it/net/aspose.words.drawing/gradientvariant/
---
## GradientVariant enumeration

Specifica la variante per un riempimento sfumato.

```csharp
public enum GradientVariant
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | Variante gradiente 'Nessuno'. |
| Variant1 | `1` | Variante del gradiente 1. |
| Variant2 | `2` | Variante gradiente 2. |
| Variant3 | `3` | Variante gradiente 3. |
| Variant4 | `4` | Variante gradiente 4. |

## Osservazioni

Corrisponde alle quattro varianti nella scheda Sfumatura nella finestra di dialogo Effetti di riempimento in Word.

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
