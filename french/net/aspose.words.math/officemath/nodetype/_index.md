---
title: OfficeMath.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words pour .NET
description: Découvrez la propriété OfficeMath NodeType qui renvoie efficacement les éléments OfficeMath, améliorant ainsi les capacités mathématiques de votre document.
type: docs
weight: 40
url: /fr/net/aspose.words.math/officemath/nodetype/
---
## OfficeMath.NodeType property

RetoursOfficeMath .

```csharp
public override NodeType NodeType { get; }
```

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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [OfficeMath](../)
* espace de noms [Aspose.Words.Math](../../../aspose.words.math/)
* Assemblée [Aspose.Words](../../../)
