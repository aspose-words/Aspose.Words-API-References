---
title: Fill.OneColorGradient
linktitle: OneColorGradient
articleTitle: OneColorGradient
second_title: Aspose.Words pour .NET
description: Découvrez comment utiliser la méthode OneColorGradient pour créer de superbes dégradés monochromes pour vos créations. Sublimez vos projets sans effort !
type: docs
weight: 220
url: /fr/net/aspose.words.drawing/fill/onecolorgradient/
---
## OneColorGradient(*[GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/), double*) {#onecolorgradient}

Définit le remplissage spécifié sur un dégradé d'une couleur.

```csharp
public void OneColorGradient(GradientStyle style, GradientVariant variant, double degree)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| style | GradientStyle | Le style dégradé[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | La variante de gradient[`GradientVariant`](../../gradientvariant/) |
| degree | Double | Le degré de dégradé. Il peut être compris entre 0,0 (foncé) et 1,0 (clair). |

## Exemples

Montre comment remplir une forme avec des dégradés.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Appliquez un remplissage dégradé d'une couleur à la forme avec la couleur de premier plan du remplissage dégradé.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Appliquer un remplissage dégradé bicolore à la forme.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Changer la couleur d'arrière-plan du remplissage dégradé.
shape.Fill.BackColor = Color.Yellow;
// Notez que "GradientAngle" est remplacé par "GradientStyle.FromCorner/GradientStyle.FromCenter"
// le remplissage en dégradé n'a aucun effet, il ne fonctionnera que pour le dégradé linéaire.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Utilisez l'option de conformité pour définir la forme à l'aide de DML si vous souhaitez obtenir « GradientStyle »,
// Propriétés « GradientVariant » et « GradientAngle » après l'enregistrement du document.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Voir également

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)

---

## OneColorGradient(*Color, [GradientStyle](../../gradientstyle/), [GradientVariant](../../gradientvariant/), double*) {#onecolorgradient_1}

Définit le remplissage spécifié sur un dégradé d'une couleur en utilisant la couleur spécifiée.

```csharp
public void OneColorGradient(Color color, GradientStyle style, GradientVariant variant, 
    double degree)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| color | Color | La couleur pour construire le dégradé. |
| style | GradientStyle | Le style dégradé[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | La variante de gradient[`GradientVariant`](../../gradientvariant/) |
| degree | Double | Le degré de dégradé. Il peut être compris entre 0,0 (foncé) et 1,0 (clair). |

## Exemples

Montre comment remplir une forme avec des dégradés.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Appliquez un remplissage dégradé d'une couleur à la forme avec la couleur de premier plan du remplissage dégradé.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Appliquer un remplissage dégradé bicolore à la forme.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Changer la couleur d'arrière-plan du remplissage dégradé.
shape.Fill.BackColor = Color.Yellow;
// Notez que "GradientAngle" est remplacé par "GradientStyle.FromCorner/GradientStyle.FromCenter"
// le remplissage en dégradé n'a aucun effet, il ne fonctionnera que pour le dégradé linéaire.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Utilisez l'option de conformité pour définir la forme à l'aide de DML si vous souhaitez obtenir « GradientStyle »,
// Propriétés « GradientVariant » et « GradientAngle » après l'enregistrement du document.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Voir également

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
