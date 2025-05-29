---
title: OfficeMathDisplayType Enum
linktitle: OfficeMathDisplayType
articleTitle: OfficeMathDisplayType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Math.OfficeMathDisplayType pour personnaliser facilement les formats d'affichage des équations pour une clarté et une présentation améliorées des documents.
type: docs
weight: 4820
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
| Display | `0` | Le bureau mathématique est affiché sur sa propre ligne. |
| Inline | `1` | Le bureau mathématique est affiché en ligne avec le texte. |

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
