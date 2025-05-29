---
title: GlowFormat.Transparency
linktitle: Transparency
articleTitle: Transparency
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Transparence de GlowFormat et ajustez facilement les effets de lueur, de l'opaque au transparent (0,0 à 1,0), pour un impact visuel saisissant. Valeur par défaut : 0,0.
type: docs
weight: 30
url: /fr/net/aspose.words.drawing/glowformat/transparency/
---
## GlowFormat.Transparency property

Obtient ou définit le degré de transparence de l'effet de lueur sous la forme d'une valeur comprise entre 0,0 (opaque) et 1,0 (clair). La valeur par défaut est 0,0.

```csharp
public double Transparency { get; set; }
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
