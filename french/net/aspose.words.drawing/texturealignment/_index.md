---
title: TextureAlignment Enum
linktitle: TextureAlignment
articleTitle: TextureAlignment
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.TextureAlignment pour un alignement précis des textures. Améliorez la conception de vos documents grâce à des options de mosaïque fluides !
type: docs
weight: 1780
url: /fr/net/aspose.words.drawing/texturealignment/
---
## TextureAlignment enumeration

Spécifie l'alignement du carrelage du remplissage de texture.

```csharp
public enum TextureAlignment
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| TopLeft | `0` | Alignement de la texture en haut à gauche. |
| Top | `1` | Alignement de la texture supérieure. |
| TopRight | `2` | Alignement de la texture en haut à droite. |
| Left | `3` | Alignement de la texture à gauche. |
| Center | `4` | Alignement de la texture centrale. |
| Right | `5` | Alignement correct de la texture. |
| BottomLeft | `6` | Alignement de la texture en bas à gauche. |
| Bottom | `7` | Alignement de la texture inférieure. |
| BottomRight | `8` | Alignement de la texture en bas à droite. |
| None | `9` | Aucun alignement de texture. |

## Exemples

Montre comment remplir et carreler la texture à l'intérieur de la forme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);

// Appliquer l'alignement de la texture au remplissage de la forme.
shape.Fill.PresetTextured(PresetTexture.Canvas);
shape.Fill.TextureAlignment = TextureAlignment.TopRight;

// Utilisez l'option de conformité pour définir la forme à l'aide de DML si vous souhaitez obtenir « TextureAlignment »
// propriété après l'enregistrement du document.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Compliance = OoxmlCompliance.Iso29500_2008_Strict };

doc.Save(ArtifactsDir + "Shape.TextureFill.docx", saveOptions);

doc = new Document(ArtifactsDir + "Shape.TextureFill.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(TextureAlignment.TopRight, shape.Fill.TextureAlignment);
Assert.AreEqual(PresetTexture.Canvas, shape.Fill.PresetTexture);
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
