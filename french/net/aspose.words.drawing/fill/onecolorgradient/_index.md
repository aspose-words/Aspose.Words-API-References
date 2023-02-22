---
title: Fill.OneColorGradient
second_title: Référence de l'API Aspose.Words pour .NET
description: Fill méthode. Définit le remplissage spécifié sur un dégradé dune seule couleur.
type: docs
weight: 160
url: /fr/net/aspose.words.drawing/fill/onecolorgradient/
---
## OneColorGradient(GradientStyle, GradientVariant, double) {#onecolorgradient}

Définit le remplissage spécifié sur un dégradé d'une seule couleur.

```csharp
public void OneColorGradient(GradientStyle style, GradientVariant variant, double degree)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| style | GradientStyle | Le style dégradé[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | La variante dégradée[`GradientVariant`](../../gradientvariant/) |
| degree | Double | Le degré de gradient. Peut être une valeur comprise entre 0,0 (sombre) et 1,0 (clair). |

### Exemples

Montre comment remplir une forme avec des dégradés.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Appliquez un remplissage dégradé à une couleur à la forme avec ForeColor de remplissage dégradé.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Appliquez un remplissage dégradé bicolore à la forme.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Change la couleur de fond du remplissage dégradé.
shape.Fill.BackColor = Color.Yellow;
// Notez que change "GradientAngle" pour "GradientStyle.FromCorner/GradientStyle.FromCenter"
// le remplissage dégradé n'a aucun effet, cela ne fonctionnera que pour le dégradé linéaire.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Utilisez l'option de conformité pour définir la forme à l'aide de DML si vous souhaitez obtenir "GradientStyle",
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

## OneColorGradient(Color, GradientStyle, GradientVariant, double) {#onecolorgradient_1}

Définit le remplissage spécifié sur un dégradé d'une couleur en utilisant la couleur spécifiée.

```csharp
public void OneColorGradient(Color color, GradientStyle style, GradientVariant variant, 
    double degree)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| color | Color | La couleur pour construire le dégradé. |
| style | GradientStyle | Le style dégradé[`GradientStyle`](../../gradientstyle/) |
| variant | GradientVariant | La variante dégradée[`GradientVariant`](../../gradientvariant/) |
| degree | Double | Le degré de gradient. Peut être une valeur comprise entre 0,0 (sombre) et 1,0 (clair). |

### Exemples

Montre comment remplir une forme avec des dégradés.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Appliquez un remplissage dégradé à une couleur à la forme avec ForeColor de remplissage dégradé.
shape.Fill.OneColorGradient(Color.Red, GradientStyle.Horizontal, GradientVariant.Variant2, 0.1);

Assert.AreEqual(Color.Red.ToArgb(), shape.Fill.ForeColor.ToArgb());
Assert.AreEqual(GradientStyle.Horizontal, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant2, shape.Fill.GradientVariant);
Assert.AreEqual(270, shape.Fill.GradientAngle);

shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// Appliquez un remplissage dégradé bicolore à la forme.
shape.Fill.TwoColorGradient(GradientStyle.FromCorner, GradientVariant.Variant4);
// Change la couleur de fond du remplissage dégradé.
shape.Fill.BackColor = Color.Yellow;
// Notez que change "GradientAngle" pour "GradientStyle.FromCorner/GradientStyle.FromCenter"
// le remplissage dégradé n'a aucun effet, cela ne fonctionnera que pour le dégradé linéaire.
shape.Fill.GradientAngle = 15;

Assert.AreEqual(Color.Yellow.ToArgb(), shape.Fill.BackColor.ToArgb());
Assert.AreEqual(GradientStyle.FromCorner, shape.Fill.GradientStyle);
Assert.AreEqual(GradientVariant.Variant4, shape.Fill.GradientVariant);
Assert.AreEqual(0, shape.Fill.GradientAngle);

// Utilisez l'option de conformité pour définir la forme à l'aide de DML si vous souhaitez obtenir "GradientStyle",
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


