---
title: Stroke.ImageBytes
second_title: Référence de l'API Aspose.Words pour .NET
description: Stroke propriété. Définit limage pour une image de trait ou un remplissage de motif.
type: docs
weight: 120
url: /fr/net/aspose.words.drawing/stroke/imagebytes/
---
## Stroke.ImageBytes property

Définit l'image pour une image de trait ou un remplissage de motif.

```csharp
public byte[] ImageBytes { get; }
```

### Exemples

Montre comment traiter les caractéristiques de trait de forme.

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
* espace de noms [Aspose.Words.Drawing](../../stroke/)
* Assemblée [Aspose.Words](../../../)


