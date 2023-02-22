---
title: Enum OfficeMathJustification
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Math.OfficeMathJustification énumération. Spécifie la justification de léquation.
type: docs
weight: 3900
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
| Right | `4` | Justification à droite du paragraphe mathématique. |
| Inline | `7` | Position en ligne de Math. |
| Default | `1` | Valeur par défautCenterGroup . |

### Exemples

Montre comment définir la mise en forme de l'affichage mathématique de bureau.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// Les nœuds OfficeMath qui sont des enfants d'autres nœuds OfficeMath sont toujours en ligne.
// Le nœud avec lequel nous travaillons est le nœud de base pour changer son emplacement et son type d'affichage.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Les formats OOXML et WML utilisent la propriété "EquationXmlEncoding".
Assert.IsNull(officeMath.EquationXmlEncoding);

// Modifier l'emplacement et le type d'affichage du nœud OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Voir également

* espace de noms [Aspose.Words.Math](../../aspose.words.math/)
* Assemblée [Aspose.Words](../../)


