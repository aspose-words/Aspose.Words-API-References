---
title: OfficeMathDisplayType Enum
linktitle: OfficeMathDisplayType
articleTitle: OfficeMathDisplayType
second_title: Aspose.Words pour .NET
description: Aspose.Words.Math.OfficeMathDisplayType énumération. Spécifie le type de format daffichage de léquation en C#.
type: docs
weight: 4130
url: /fr/net/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enumeration

Spécifie le type de format d'affichage de l'équation.

```csharp
public enum OfficeMathDisplayType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Display | `0` | Office Math est affiché sur sa propre ligne. |
| Inline | `1` | Office Math s'affiche en ligne avec le texte. |

## Exemples

Montre comment définir le formatage de l’affichage des mathématiques de bureau.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// Les nœuds OfficeMath qui sont des enfants d'autres nœuds OfficeMath sont toujours en ligne.
// Le nœud avec lequel nous travaillons est le nœud de base pour changer son emplacement et son type d'affichage.
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
