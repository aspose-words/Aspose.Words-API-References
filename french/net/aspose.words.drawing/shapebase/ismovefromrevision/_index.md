---
title: ShapeBase.IsMoveFromRevision
second_title: Référence de l'API Aspose.Words pour .NET
description: ShapeBase propriété. Retours vrai si cet objet a été déplacé supprimé dans Microsoft Word alors que le suivi des modifications était activé.
type: docs
weight: 310
url: /fr/net/aspose.words.drawing/shapebase/ismovefromrevision/
---
## ShapeBase.IsMoveFromRevision property

Retours **vrai** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé.

```csharp
public bool IsMoveFromRevision { get; }
```

### Exemples

Montre comment identifier les formes de révision de déplacement.

```csharp
// Une révision de déplacement se produit lorsque nous déplaçons un élément dans le corps du document en le coupant-collant dans Microsoft Word alors que
// suivi des modifications. Si nous impliquons une forme en ligne dans un tel mouvement de texte, cette forme sera également une révision.
// Le copier-coller ou le déplacement de formes flottantes ne crée pas de révisions de déplacement.
Document doc = new Document(MyDir + "Revision shape.docx");

// Les révisions de déplacement consistent en des paires de révisions "Déplacer de" et "Déplacer vers". Nous nous sommes déplacés dans ce document sous une forme,
// mais jusqu'à ce que nous acceptions ou rejetions la révision de déplacement, il y aura deux instances de cette forme.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Il s'agit de la révision "Déplacer vers", qui est la forme à sa destination d'arrivée.
// Si nous acceptons la révision, cette forme de révision "Déplacer vers" disparaîtra,
// et la forme de révision "Move from" restera.
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// Il s'agit de la révision "Move from", qui est la forme à son emplacement d'origine.
// Si nous acceptons la révision, cette forme de révision "Move from" disparaîtra,
// et la forme de révision "Déplacer vers" restera.
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../shapebase/)
* Assemblée [Aspose.Words](../../../)


