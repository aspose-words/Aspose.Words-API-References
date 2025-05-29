---
title: ShapeBase.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété IsMoveToRevision de ShapeBase améliore votre expérience Microsoft Word en suivant les mouvements des objets de manière transparente pendant les modifications.
type: docs
weight: 350
url: /fr/net/aspose.words.drawing/shapebase/ismovetorevision/
---
## ShapeBase.IsMoveToRevision property

Retours`vrai` si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé.

```csharp
public bool IsMoveToRevision { get; }
```

## Exemples

Montre comment identifier les formes de révision de déplacement.

```csharp
// Une révision de déplacement se produit lorsque nous déplaçons un élément dans le corps du document en le coupant et en le collant dans Microsoft Word pendant
// Suivi des modifications. Si nous impliquons une forme en ligne dans un tel mouvement de texte, cette forme sera également une révision.
// Copier-coller ou déplacer des formes flottantes ne crée pas de révisions de déplacement.
Document doc = new Document(MyDir + "Revision shape.docx");

// Les révisions de déplacement sont composées de paires de révisions « Déplacer de » et « Déplacer vers ». Dans ce document, nous avons déplacé une forme.
// mais jusqu'à ce que nous acceptions ou rejetions la révision du déplacement, il y aura deux instances de cette forme.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Il s'agit de la révision « Déplacer vers », qui correspond à la forme à sa destination d'arrivée.
// Si nous acceptons la révision, cette forme de révision « Déplacer vers » disparaîtra,
// et la forme de révision « Déplacer depuis » restera.
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// Il s'agit de la révision « Déplacer depuis », qui correspond à la forme à son emplacement d'origine.
// Si nous acceptons la révision, cette forme de révision « Déplacer depuis » disparaîtra,
// et la forme de révision « Déplacer vers » restera.
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
