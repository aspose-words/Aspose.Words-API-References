---
title: GlowFormat.Color
linktitle: Color
articleTitle: Color
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Couleur GlowFormat pour personnaliser vos effets lumineux. Définissez facilement des couleurs vives pour un impact visuel saisissant. La valeur par défaut est le noir.
type: docs
weight: 10
url: /fr/net/aspose.words.drawing/glowformat/color/
---
## GlowFormat.Color property

Obtient ou définit unColor objet qui représente la couleur d'un effet de lueur. La valeur par défaut estBlack .

```csharp
public Color Color { get; set; }
```

## Exemples

Montre comment interagir avec l'effet de forme de lueur.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Glow.Color = Color.Salmon;
shape.Glow.Radius = 30;
shape.Glow.Transparency = 0.15;

doc.Save(ArtifactsDir + "Shape.Glow.docx");

doc = new Document(ArtifactsDir + "Shape.Glow.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(Color.FromArgb(217, 250, 128, 114).ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(30, shape.Glow.Radius);
Assert.AreEqual(0.15d, shape.Glow.Transparency, 0.01d);

shape.Glow.Remove();

Assert.AreEqual(Color.Black.ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(0, shape.Glow.Radius);
Assert.AreEqual(0, shape.Glow.Transparency);
```

### Voir également

* class [GlowFormat](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
