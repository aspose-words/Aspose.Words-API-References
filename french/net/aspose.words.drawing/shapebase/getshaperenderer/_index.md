---
title: ShapeBase.GetShapeRenderer
linktitle: GetShapeRenderer
articleTitle: GetShapeRenderer
second_title: Aspose.Words pour .NET
description: ShapeBase GetShapeRenderer méthode. Crée et renvoie un objet qui peut être utilisé pour restituer cette forme en image en C#.
type: docs
weight: 660
url: /fr/net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

Crée et renvoie un objet qui peut être utilisé pour restituer cette forme en image.

```csharp
public ShapeRenderer GetShapeRenderer()
```

### Return_Value

L'objet de rendu pour cette forme.

## Remarques

Cette méthode invoque simplement le[`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer/) constructeur et passe cet objet en paramètre.

## Exemples

Montre comment utiliser un moteur de rendu de formes pour exporter des formes vers des fichiers dans le système de fichiers local.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Il y a 7 formes dans le document, dont une forme de groupe avec 2 formes enfants.
// Nous allons rendre chaque forme dans un fichier image dans le système de fichiers local
// en ignorant les formes de groupe puisqu'elles n'ont pas d'apparence.
// Cela produira 6 fichiers image.
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### Voir également

* class [ShapeRenderer](../../../aspose.words.rendering/shaperenderer/)
* class [ShapeBase](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
