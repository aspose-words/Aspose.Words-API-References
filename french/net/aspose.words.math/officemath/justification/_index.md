---
title: OfficeMath.Justification
linktitle: Justification
articleTitle: Justification
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Justification OfficeMath pour personnaliser et définir facilement votre alignement Office Math. Améliorez la présentation de vos documents sans effort !
type: docs
weight: 20
url: /fr/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

Obtient/définit la justification Office Math.

```csharp
public OfficeMathJustification Justification { get; set; }
```

## Remarques

La justification ne peut pas être définie sur le type de format d'affichage Office MathInline.

La justification en ligne ne peut pas être définie sur le type de format d'affichage Office MathDisplay.

Correspondant[`DisplayType`](../displaytype/) doit être défini avant de définir la justification Office Math.

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

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* espace de noms [Aspose.Words.Math](../../../aspose.words.math/)
* Assemblée [Aspose.Words](../../../)
