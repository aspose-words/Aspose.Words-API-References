---
title: Shape.HasSmartArt
linktitle: HasSmartArt
articleTitle: HasSmartArt
second_title: Aspose.Words pour .NET
description: Découvrez si votre forme comporte un objet SmartArt avec la propriété HasSmartArt. Libérez vos possibilités de conception créative pour vos projets !
type: docs
weight: 100
url: /fr/net/aspose.words.drawing/shape/hassmartart/
---
## Shape.HasSmartArt property

Retours`vrai` si cela[`Shape`](../) a un objet SmartArt.

```csharp
public bool HasSmartArt { get; }
```

## Exemples

Montre comment compter le nombre de formes dans un document avec des objets SmartArt.

```csharp
Document doc = new Document(MyDir + "SmartArt.docx");

int numberOfSmartArtShapes = doc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Count(shape => shape.HasSmartArt);

Assert.AreEqual(2, numberOfSmartArtShapes);
```

### Voir également

* class [Shape](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
