---
title: Color2
second_title: Référence de l'API Aspose.Words pour .NET
description: Définit une deuxième couleur pour un trait.
type: docs
weight: 30
url: /fr/net/aspose.words.drawing/stroke/color2/
---
## Stroke.Color2 property

Définit une deuxième couleur pour un trait.

```csharp
public Color Color2 { get; set; }
```

### Remarques

La valeur par défaut pour un[`Shape`](../../shape) est White.

### Exemples

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

* class [Stroke](../../stroke)
* espace de noms [Aspose.Words.Drawing](../../stroke)
* Assemblée [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->