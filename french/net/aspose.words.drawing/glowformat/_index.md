---
title: GlowFormat Class
linktitle: GlowFormat
articleTitle: GlowFormat
second_title: Aspose.Words pour .NET
description: Explorez la classe Aspose.Words.Drawing.GlowFormat pour sublimer vos documents avec de superbes effets lumineux. Sublimez votre design grâce à des options de mise en forme uniques !
type: docs
weight: 1300
url: /fr/net/aspose.words.drawing/glowformat/
---
## GlowFormat class

Représente le formatage de la lueur d'un objet.

```csharp
public class GlowFormat
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Color](../../aspose.words.drawing/glowformat/color/) { get; set; } | Obtient ou définit unColor objet qui représente la couleur d'un effet de lueur. La valeur par défaut estBlack . |
| [Radius](../../aspose.words.drawing/glowformat/radius/) { get; set; } | Obtient ou définit une valeur double qui représente la longueur du rayon pour un effet de lueur en points (pt). La valeur par défaut est 0,0. |
| [Transparency](../../aspose.words.drawing/glowformat/transparency/) { get; set; } | Obtient ou définit le degré de transparence de l'effet de lueur sous la forme d'une valeur comprise entre 0,0 (opaque) et 1,0 (clair). La valeur par défaut est 0,0. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Remove](../../aspose.words.drawing/glowformat/remove/)() | Supprime`GlowFormat` de l'objet parent. |

## Remarques

Utilisez le[`Glow`](../shapebase/glow/) propriété pour accéder aux propriétés de lueur d'un objet. Vous ne créez pas d'instances de la`GlowFormat` classe directement.

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

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
