---
title: TextDmlEffect Enum
linktitle: TextDmlEffect
articleTitle: TextDmlEffect
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.TextDmlEffect pour enrichir les séquences de texte avec des effets DML dynamiques. Améliorez la présentation de vos documents sans effort !
type: docs
weight: 7260
url: /fr/net/aspose.words/textdmleffect/
---
## TextDmlEffect enumeration

Effet de texte Dml pour les exécutions de texte.

```csharp
public enum TextDmlEffect
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Glow | `0` | Effet de lueur, dans lequel un contour flou de couleur est ajouté à l'extérieur des bords de l'objet. |
| Fill | `1` | Effet de superposition de remplissage. |
| Shadow | `2` | Effet d'ombre. |
| Outline | `3` | Effet de contour. |
| Effect3D | `4` | Effet 3D. |
| Reflection | `5` | Effet de réflexion. |

## Exemples

Montre comment vérifier si une exécution affiche un effet de texte DrawingML.

```csharp
Document doc = new Document(MyDir + "DrawingML text effects.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.True(runs[0].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[1].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[2].Font.HasDmlEffect(TextDmlEffect.Reflection));
Assert.True(runs[3].Font.HasDmlEffect(TextDmlEffect.Effect3D));
Assert.True(runs[4].Font.HasDmlEffect(TextDmlEffect.Fill));
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
