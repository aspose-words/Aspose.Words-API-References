---
title: OfficeMath.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words pour .NET
description: Découvrez la propriété OfficeMath ParentParagraph pour accéder facilement au paragraphe parent de n'importe quel nœud, améliorant ainsi la mise en forme et la structure de votre document.
type: docs
weight: 50
url: /fr/net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

Récupère le parent[`Paragraph`](../../../aspose.words/paragraph/) de ce nœud.

```csharp
public Paragraph ParentParagraph { get; }
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* espace de noms [Aspose.Words.Math](../../../aspose.words.math/)
* Assemblée [Aspose.Words](../../../)
