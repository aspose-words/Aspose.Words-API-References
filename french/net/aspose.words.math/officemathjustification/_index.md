---
title: OfficeMathJustification Enum
linktitle: OfficeMathJustification
articleTitle: OfficeMathJustification
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Math.OfficeMathJustification pour un alignement précis des équations. Améliorez la clarté de votre document grâce à des options de justification optimales.
type: docs
weight: 4830
url: /fr/net/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enumeration

Spécifie la justification de l'équation.

```csharp
public enum OfficeMathJustification
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| CenterGroup | `1` | Justifie les instances de texte mathématique à gauche les unes par rapport aux autres et centre le groupe de texte mathématique (le paragraphe mathématique) par rapport à la page. |
| Center | `2` | Centre chaque instance de texte mathématique individuellement par rapport aux marges. |
| Left | `3` | Justification à gauche du paragraphe mathématique. |
| Right | `4` | Justification correcte du paragraphe mathématique. |
| Inline | `7` | Position en ligne de Math. |
| Default | `1` | Valeur par défautCenterGroup . |

## Exemples

Montre comment définir la mise en forme de l'affichage mathématique du bureau.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Les nœuds OfficeMath qui sont des enfants d'autres nœuds OfficeMath sont toujours en ligne.
// Le nœud avec lequel nous travaillons est le nœud de base pour modifier son emplacement et son type d'affichage.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Modifiez l'emplacement et le type d'affichage du nœud OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Voir également

* espace de noms [Aspose.Words.Math](../../aspose.words.math/)
* Assemblée [Aspose.Words](../../)
