---
title: ShapeBase.GetShapeRenderer
second_title: Référence de l'API Aspose.Words pour .NET
description: ShapeBase méthode. Crée et renvoie un objet qui peut être utilisé pour rendre cette forme dans une image.
type: docs
weight: 600
url: /fr/net/aspose.words.drawing/shapebase/getshaperenderer/
---
## ShapeBase.GetShapeRenderer method

Crée et renvoie un objet qui peut être utilisé pour rendre cette forme dans une image.

```csharp
public ShapeRenderer GetShapeRenderer()
```

### Return_Value

Objet de rendu pour cette forme.

### Remarques

Cette méthode invoque simplement le[`ShapeRenderer`](../../../aspose.words.rendering/shaperenderer/) constructeur et passe cet objet en paramètre.

### Exemples

Montre comment utiliser un rendu de forme pour exporter des formes vers des fichiers dans le système de fichiers local.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// Il y a 7 formes dans le document, y compris une forme de groupe avec 2 formes enfants.
// Nous rendrons chaque forme dans un fichier image dans le système de fichiers local
// tout en ignorant les formes de groupe puisqu'elles n'ont pas d'apparence.
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
* espace de noms [Aspose.Words.Drawing](../../shapebase/)
* Assemblée [Aspose.Words](../../../)


