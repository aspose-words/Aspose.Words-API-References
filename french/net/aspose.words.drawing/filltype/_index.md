---
title: FillType Enum
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.FillType pour améliorer vos objets remplissables avec des types de remplissage polyvalents pour une conception de document améliorée.
type: docs
weight: 1280
url: /fr/net/aspose.words.drawing/filltype/
---
## FillType enumeration

Spécifie le type de remplissage pour un objet remplissable.

```csharp
public enum FillType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Solid | `1` | Remplissage solide. |
| Patterned | `2` | Remplissage à motifs. |
| Gradient | `3` | Remplissage dégradé. |
| Textured | `4` | Remplissage texturé. |
| Background | `5` | Le remplissage est le même que l'arrière-plan. |
| Picture | `6` | Remplissage d'image. |

## Exemples

Montre comment reconvertir n'importe quel remplissage en remplissage solide.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Obtenir l'objet Fill pour la police de la première exécution.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Vérifiez les propriétés de remplissage de la police.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Changez le type de remplissage en Solide avec une couleur verte uniforme.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
