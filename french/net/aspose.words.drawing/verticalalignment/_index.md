---
title: VerticalAlignment Enum
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.VerticalAlignment pour un alignement vertical précis des blocs de texte et des tableaux dans vos documents. Améliorez le contrôle de la mise en page !
type: docs
weight: 1790
url: /fr/net/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enumeration

Spécifie l'alignement vertical d'une forme flottante, d'un cadre de texte ou d'un tableau flottant.

```csharp
public enum VerticalAlignment
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | L'objet est explicitement positionné, généralement en utilisant son**Haut** propriété. |
| Top | `1` | Spécifie que l'objet doit être en haut de la base d'alignement vertical. |
| Center | `2` | Spécifie que l'objet doit être centré par rapport à la base d'alignement vertical. |
| Bottom | `3` | Spécifie que l'objet doit être au bas de la base d'alignement vertical. |
| Inside | `4` | Spécifie que l'objet doit être à l'intérieur de la base d'alignement horizontal. |
| Outside | `5` | Spécifie que l'objet doit être en dehors de la base d'alignement vertical. |
| Inline | `-1` | Non documenté. Semble être une valeur possible pour les paragraphes et tableaux flottants. |
| Default | `0` | Identique àNone . |

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

* property [VerticalAlignment](../shapebase/verticalalignment/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
