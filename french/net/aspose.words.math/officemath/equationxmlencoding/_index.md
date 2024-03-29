---
title: OfficeMath.EquationXmlEncoding
second_title: Référence de l'API Aspose.Words pour .NET
description: OfficeMath propriété. Obtient/définit un encodage qui a été utilisé pour encoder léquation XML si cet objet mathématique de bureau est lu à partir de equation XML. Nous utilisons lencodage lors de lenregistrement dun document pour écrire dans le même encodage quil a été lu.
type: docs
weight: 20
url: /fr/net/aspose.words.math/officemath/equationxmlencoding/
---
## OfficeMath.EquationXmlEncoding property

Obtient/définit un encodage qui a été utilisé pour encoder l'équation XML, si cet objet mathématique de bureau est lu à partir de equation XML. Nous utilisons l'encodage lors de l'enregistrement d'un document pour écrire dans le même encodage qu'il a été lu.

```csharp
public Encoding EquationXmlEncoding { get; set; }
```

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

* class [OfficeMath](../)
* espace de noms [Aspose.Words.Math](../../officemath/)
* Assemblée [Aspose.Words](../../../)


