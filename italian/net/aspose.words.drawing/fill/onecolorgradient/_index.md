---
title: Fill.OneColorGradient
linktitle: OneColorGradient
articleTitle: OneColorGradient
second_title: Aspose.Words per .NET
description: Scopri come utilizzare il metodo OneColorGradient per creare splendide sfumature monocromatiche per i tuoi progetti. Migliora i tuoi progetti senza sforzo!
type: docs
weight: 220
url: /it/net/aspose.words.drawing/fill/onecolorgradient/
---
## OneColorGradient(*[GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/), double*) {#onecolorgradient}

Imposta il riempimento specificato su un gradiente di un solo colore.

```csharp
public void OneColorGradient(GradientStyle style, GradientVariant variant, double degree)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| style | GradientStyle | Lo stile sfumato[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | La variante del gradiente[`GradientVariant`](../../gradientvariant/) |
| degree | Double | Il grado di sfumatura. Può essere un valore compreso tra 0,0 (scuro) e 1,0 (chiaro). |

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

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)

---

## OneColorGradient(*Color, [GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/), double*) {#onecolorgradient_1}

Imposta il riempimento specificato su un gradiente monocolore utilizzando il colore specificato.

```csharp
public void OneColorGradient(Color color, GradientStyle style, GradientVariant variant, 
    double degree)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| color | Color | Il colore per creare il gradiente. |
| style | GradientStyle | Lo stile sfumato[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | La variante del gradiente[`GradientVariant`](../../gradientvariant/) |
| degree | Double | Il grado di sfumatura. Può essere un valore compreso tra 0,0 (scuro) e 1,0 (chiaro). |

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

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
