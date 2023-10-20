---
title: ShapeBase.ZOrder
linktitle: ZOrder
articleTitle: ZOrder
second_title: Aspose.Words pour .NET
description: ShapeBase ZOrder propriété. Détermine lordre daffichage des formes qui se chevauchent en C#.
type: docs
weight: 610
url: /fr/net/aspose.words.drawing/shapebase/zorder/
---
## ShapeBase.ZOrder property

Détermine l'ordre d'affichage des formes qui se chevauchent.

```csharp
public int ZOrder { get; set; }
```

## Remarques

N'a d'effet que sur les formes de niveau supérieur.

La valeur par défaut est 0.

Le nombre représente la priorité d'empilement. Une forme avec un nombre plus élevé sera display comme si elle chevauchait (devant) une forme avec un nombre inférieur.

L'ordre des formes qui se chevauchent est indépendant pour les formes dans l'en-tête et dans le texte main du document.

L'ordre d'affichage des formes enfants dans une forme de groupe est déterminé par leur order à l'intérieur de la forme de groupe.

## Exemples

Montre comment manipuler l’ordre des formes.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insère trois rectangles de couleurs différentes qui se chevauchent partiellement.
// Lorsque nous insérons une forme qui chevauche une autre forme, Aspose.Words place la nouvelle forme au-dessus de l'ancienne.
// Le rectangle vert clair chevauchera le rectangle bleu clair et l'obscurcira partiellement,
// et le rectangle bleu clair masquera le rectangle orange.
Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);
shape.FillColor = Color.Orange;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 150,
    RelativeVerticalPosition.TopMargin, 150, 200, 200, WrapType.None);
shape.FillColor = Color.LightBlue;

shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 200, 200, WrapType.None);
shape.FillColor = Color.LightGreen;

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

// La propriété "ZOrder" d'une forme détermine sa priorité d'empilement parmi les autres formes superposées.
// Si deux formes superposées ont des valeurs "ZOrder" différentes,
// Microsoft Word placera la forme avec une valeur plus élevée sur la forme avec la valeur la plus faible. 
// Définissez les valeurs "ZOrder" de nos formes pour placer le premier rectangle orange sur le deuxième bleu clair
// et le deuxième rectangle bleu clair sur le troisième rectangle vert clair.
// Cela inversera leur ordre d'empilement d'origine.
shapes[0].ZOrder = 3;
shapes[1].ZOrder = 2;
shapes[2].ZOrder = 1;

doc.Save(ArtifactsDir + "Shape.ZOrder.docx");
```

### Voir également

* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
