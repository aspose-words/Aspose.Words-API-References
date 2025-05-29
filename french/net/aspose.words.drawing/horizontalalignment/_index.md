---
title: HorizontalAlignment Enum
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.HorizontalAlignment pour un contrôle précis de l'alignement horizontal des blocs de texte et tableaux flottants. Améliorez la mise en page de vos documents !
type: docs
weight: 1360
url: /fr/net/aspose.words.drawing/horizontalalignment/
---
## HorizontalAlignment enumeration

Spécifie l'alignement horizontal d'une forme flottante, d'un cadre de texte ou d'un tableau flottant.

```csharp
public enum HorizontalAlignment
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | L'objet est explicitement positionné, généralement en utilisant son**Gauche** propriété. |
| Default | `0` | Identique àNone . |
| Left | `1` | Spécifie que l'objet doit être aligné à gauche sur la base d'alignement horizontal. |
| Center | `2` | Spécifie que l'objet doit être centré par rapport à la base d'alignement horizontal. |
| Right | `3` | Spécifie que l'objet doit être aligné à droite sur la base d'alignement horizontal. |
| Inside | `4` | Spécifie que l'objet doit être à l'intérieur de la base d'alignement horizontal. |
| Outside | `5` | Spécifie que l'objet doit être en dehors de la base d'alignement horizontal. |

## Exemples

Montre comment insérer une image flottante au centre d'une page.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez une image flottante qui apparaîtra derrière le texte superposé et alignez-la au centre de la page.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### Voir également

* property [HorizontalAlignment](../shapebase/horizontalalignment/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
