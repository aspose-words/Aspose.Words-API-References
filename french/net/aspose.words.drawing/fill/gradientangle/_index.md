---
title: Fill.GradientAngle
linktitle: GradientAngle
articleTitle: GradientAngle
second_title: Aspose.Words pour .NET
description: Ajustez la propriété GradientAngle pour personnaliser l'angle de remplissage de votre dégradé, améliorant ainsi sans effort la profondeur et l'attrait visuel de votre conception.
type: docs
weight: 100
url: /fr/net/aspose.words.drawing/fill/gradientangle/
---
## Fill.GradientAngle property

Obtient ou définit l'angle du remplissage du dégradé.

```csharp
public double GradientAngle { get; set; }
```

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

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
