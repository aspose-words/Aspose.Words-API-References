---
title: OfficeMath.ParentParagraph
second_title: Référence de l'API Aspose.Words pour .NET
description: OfficeMath propriété. Récupère le parentParagraph de ce nœud.
type: docs
weight: 50
url: /fr/net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

Récupère le parent[`Paragraph`](../../../aspose.words/paragraph/) de ce nœud.

```csharp
public Paragraph ParentParagraph { get; }
```

### Exemples

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* espace de noms [Aspose.Words.Math](../../officemath/)
* Assemblée [Aspose.Words](../../../)


