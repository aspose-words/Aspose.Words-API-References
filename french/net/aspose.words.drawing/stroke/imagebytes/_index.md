---
title: Stroke.ImageBytes
linktitle: ImageBytes
articleTitle: ImageBytes
second_title: Aspose.Words pour .NET
description: Découvrez comment utiliser la propriété ImageBytes pour créer de superbes images de traits et des motifs de remplissage uniques pour vos créations. Améliorez vos visuels dès aujourd'hui !
type: docs
weight: 160
url: /fr/net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

Définit l'image pour une image de trait ou un remplissage de motif.

```csharp
public byte[] ImageBytes { get; }
```

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
