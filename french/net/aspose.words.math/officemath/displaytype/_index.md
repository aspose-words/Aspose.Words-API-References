---
title: OfficeMath.DisplayType
second_title: Référence de l'API Aspose.Words pour .NET
description: OfficeMath propriété. Obtient/définit le type de format daffichage Office Math qui indique si une équation est affichée en ligne avec le texte ou affichée sur sa propre ligne.
type: docs
weight: 10
url: /fr/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

Obtient/définit le type de format d'affichage Office Math qui indique si une équation est affichée en ligne avec le texte ou affichée sur sa propre ligne.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

### Remarques

Le type de format d’affichage n’a d’effet que pour Office Math de niveau supérieur.

Le type de format d'affichage renvoyé est toujoursInline pour Office Math imbriqué.

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* espace de noms [Aspose.Words.Math](../../officemath/)
* Assemblée [Aspose.Words](../../../)


