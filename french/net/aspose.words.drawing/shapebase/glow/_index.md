---
title: ShapeBase.Glow
linktitle: Glow
articleTitle: Glow
second_title: Aspose.Words pour .NET
description: Sublimez vos créations avec ShapeBase Glow ! Obtenez des effets lumineux époustouflants pour vos formes et sublimez vos projets visuels sans effort.
type: docs
weight: 200
url: /fr/net/aspose.words.drawing/shapebase/glow/
---
## ShapeBase.Glow property

Obtient le formatage de lueur pour la forme.

```csharp
public GlowFormat Glow { get; }
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

* class [GlowFormat](../../glowformat/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
