---
title: Fill.TwoColorGradient
second_title: Référence de l'API Aspose.Words pour .NET
description: Fill méthode. Définit le remplissage spécifié sur un dégradé bicolore.
type: docs
weight: 270
url: /fr/net/aspose.words.drawing/fill/twocolorgradient/
---
## TwoColorGradient(GradientStyle, GradientVariant) {#twocolorgradient}

Définit le remplissage spécifié sur un dégradé bicolore.

```csharp
public void TwoColorGradient(GradientStyle style, GradientVariant variant)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| style | GradientStyle | Le style dégradé[`GradientStyle`](../../gradientstyle/). |
| variant | GradientVariant | La variante dégradée[`GradientVariant`](../../gradientvariant/) |

### Exemples

Montre comment remplir une forme avec des dégradés.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Applique un remplissage dégradé d'une couleur à la forme avec ForeColor du remplissage dégradé.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Applique un remplissage dégradé bicolore à la forme.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Change la BackColor du remplissage dégradé.
shape.Fill.BackColor = Color.Yellow;
// Notez que change "GradientAngle" pour "GradientStyle.FromCorner/GradientStyle.FromCenter"
// Le remplissage dégradé n'obtient aucun effet, cela ne fonctionnera que pour les dégradés linéaires.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Utilisez l'option de conformité pour définir la forme en utilisant DML si vous souhaitez obtenir "GradientStyle",
// Propriétés "GradientVariant" et "GradientAngle" après l'enregistrement du document.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Voir également

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../fill/)
* Assemblée [Aspose.Words](../../../)

---

## TwoColorGradient(Color, Color, GradientStyle, GradientVariant) {#twocolorgradient_1}

Définit le remplissage spécifié sur un dégradé bicolore.

```csharp
public void TwoColorGradient(Color color1, Color color2, GradientStyle style, 
    GradientVariant variant)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| color1 | Color | La première couleur pour construire le dégradé. |
| color2 | Color | La deuxième couleur pour construire le dégradé. |
| style | GradientStyle | Le style dégradé[`GradientStyle`](../../gradientstyle/). |
| variant | GradientVariant | La variante dégradée[`GradientVariant`](../../gradientvariant/) |

### Exemples

Montre comment remplir une forme avec des dégradés.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Applique un remplissage dégradé d'une couleur à la forme avec ForeColor du remplissage dégradé.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Applique un remplissage dégradé bicolore à la forme.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Change la BackColor du remplissage dégradé.
shape.Fill.BackColor = Color.Yellow;
// Notez que change "GradientAngle" pour "GradientStyle.FromCorner/GradientStyle.FromCenter"
// Le remplissage dégradé n'obtient aucun effet, cela ne fonctionnera que pour les dégradés linéaires.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Utilisez l'option de conformité pour définir la forme en utilisant DML si vous souhaitez obtenir "GradientStyle",
// Propriétés "GradientVariant" et "GradientAngle" après l'enregistrement du document.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.GradientFill.docx", saveOptions);
```

### Voir également

* enum [GradientStyle](../../gradientstyle/)
* enum [GradientVariant](../../gradientvariant/)
* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../fill/)
* Assemblée [Aspose.Words](../../../)


