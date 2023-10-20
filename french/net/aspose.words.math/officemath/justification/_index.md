---
title: OfficeMath.Justification
linktitle: Justification
articleTitle: Justification
second_title: Aspose.Words pour .NET
description: OfficeMath Justification propriété. Obtient/définit la justification Office Math en C#.
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

La justification ne peut pas être définie sur Office Math avec le type de format d'affichageInline.

La justification en ligne ne peut pas être définie sur Office Math avec le type de format d'affichageDisplay.

Correspondant[`DisplayType`](../displaytype/) doit être défini avant de définir la justification Office Math.

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

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* espace de noms [Aspose.Words.Math](../../../aspose.words.math/)
* Assemblée [Aspose.Words](../../../)
