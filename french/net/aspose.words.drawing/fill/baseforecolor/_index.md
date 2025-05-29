---
title: Fill.BaseForeColor
linktitle: BaseForeColor
articleTitle: BaseForeColor
second_title: Aspose.Words pour .NET
description: Découvrez la propriété BaseForeColor pour accéder à un objet Color représentant la véritable couleur de premier plan de votre remplissage, améliorant ainsi la clarté et l'attrait de votre conception.
type: docs
weight: 40
url: /fr/net/aspose.words.drawing/fill/baseforecolor/
---
## Fill.BaseForeColor property

Obtient un objet Color qui représente la couleur de premier plan de base pour le remplissage sans aucun modificateur.

```csharp
public Color BaseForeColor { get; }
```

## Exemples

Montre comment obtenir une couleur de premier plan sans modificateurs.

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

### Voir également

* class [Fill](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
