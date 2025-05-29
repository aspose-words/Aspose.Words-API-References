---
title: GlowFormat.Radius
linktitle: Radius
articleTitle: Radius
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Rayon GlowFormat pour personnaliser vos effets de lueur. Ajustez le rayon en points pour des améliorations visuelles exceptionnelles. Valeur par défaut : 0,0.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/glowformat/radius/
---
## GlowFormat.Radius property

Obtient ou définit une valeur double qui représente la longueur du rayon pour un effet de lueur en points (pt). La valeur par défaut est 0,0.

```csharp
public double Radius { get; set; }
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
