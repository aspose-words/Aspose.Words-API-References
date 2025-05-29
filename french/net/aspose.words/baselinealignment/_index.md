---
title: BaselineAlignment Enum
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.BaselineAlignment pour un positionnement précis des polices. Améliorez la mise en forme de vos documents grâce à des options d'alignement vertical optimales.
type: docs
weight: 130
url: /fr/net/aspose.words/baselinealignment/
---
## BaselineAlignment enumeration

Spécifie la position verticale des polices sur une ligne.

```csharp
public enum BaselineAlignment
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Top | `0` | S'aligne en haut de chaque police. |
| Center | `1` | Aligne les points centraux de chaque police. |
| Baseline | `2` | S'aligne sur la ligne de base du paragraphe. |
| Bottom | `3` | S'aligne au bas de chaque police. |
| Auto | `4` | La ligne de base est ajustée automatiquement. |

## Exemples

Montre comment définir la position verticale des polices sur une ligne.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
if (format.BaselineAlignment == BaselineAlignment.Auto)
{                
    format.BaselineAlignment = BaselineAlignment.Top;
}

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
