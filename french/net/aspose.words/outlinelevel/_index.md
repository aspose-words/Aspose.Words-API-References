---
title: OutlineLevel Enum
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.OutlineLevel pour gérer facilement les niveaux de plan de paragraphe dans vos documents pour une organisation et une clarté améliorées.
type: docs
weight: 5060
url: /fr/net/aspose.words/outlinelevel/
---
## OutlineLevel enumeration

Spécifie le niveau de plan d'un paragraphe dans le document.

```csharp
public enum OutlineLevel
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Level1 | `0` | Le paragraphe est au niveau de plan 1 (niveau le plus élevé). |
| Level2 | `1` | Le paragraphe est au niveau de plan 2. |
| Level3 | `2` | Le paragraphe est au niveau de plan 3. |
| Level4 | `3` | Le paragraphe est au niveau de plan 4. |
| Level5 | `4` | Le paragraphe est au niveau de plan 5. |
| Level6 | `5` | Le paragraphe est au niveau du plan 6. |
| Level7 | `6` | Le paragraphe est au niveau du plan 7. |
| Level8 | `7` | Le paragraphe est au niveau de plan 8. |
| Level9 | `8` | Le paragraphe est au niveau du plan 9. |
| BodyText | `9` | Le paragraphe est au niveau du texte principal. |

## Exemples

Montre comment configurer les niveaux de plan de paragraphe pour créer du texte réductible.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Chaque paragraphe a un OutlineLevel, qui peut être n'importe quel nombre de 1 à 9, ou la valeur par défaut « BodyText ».
// La définition de la propriété sur l'une des valeurs numérotées affichera une flèche vers la gauche
// du début du paragraphe.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// Le niveau 1 est le niveau le plus élevé. Si un paragraphe de niveau inférieur se trouve sous un paragraphe de niveau supérieur,
// réduire le paragraphe de niveau supérieur réduira le paragraphe de niveau inférieur.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// Deux paragraphes du même niveau ne s'effondreront pas l'un l'autre,
// et les flèches ne réduisent pas les paragraphes vers lesquels elles pointent.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// La valeur par défaut de « BodyText » est la plus basse à laquelle un paragraphe de n'importe quel niveau peut se réduire.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
