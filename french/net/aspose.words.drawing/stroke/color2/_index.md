---
title: Stroke.Color2
linktitle: Color2
articleTitle: Color2
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Stroke Color2  améliorez vos créations avec une deuxième couleur de trait personnalisable pour des visuels dynamiques et accrocheurs.
type: docs
weight: 60
url: /fr/net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

Définit une deuxième couleur pour un trait.

```csharp
public Color Color2 { get; set; }
```

## Remarques

La valeur par défaut pour un[`Shape`](../../shape/) is White .

## Exemples

Montre comment traiter les fonctions de trait de forme.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Stroke stroke = shape.Stroke;

// Les traits peuvent avoir deux couleurs, qui sont utilisées pour créer un motif défini par des données d'image bicolores.
// Les traits avec une seule couleur n'utilisent pas la propriété Color2.
Assert.AreEqual(Color.FromArgb(255, 128, 0, 0), stroke.Color);
Assert.AreEqual(Color.FromArgb(255, 255, 255, 0), stroke.Color2);

Assert.NotNull(stroke.ImageBytes);
File.WriteAllBytes(ArtifactsDir + "Drawing.StrokePattern.png", stroke.ImageBytes);
```

### Voir également

* class [Stroke](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
