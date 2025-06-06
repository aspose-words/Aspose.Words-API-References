---
title: Shape.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words pour .NET
description: Découvrez si une forme contient des données d'image ou des liens vers une image grâce à la propriété HasImage. Améliorez vos créations sans effort !
type: docs
weight: 90
url: /fr/net/aspose.words.drawing/shape/hasimage/
---
## Shape.HasImage property

Retours`vrai` si la forme contient des octets d'image ou lie une image.

```csharp
public bool HasImage { get; }
```

## Exemples

Montre comment supprimer toutes les formes avec des images d'un document.

```csharp
Document doc = new Document(MyDir + "Images.docx");
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.OfType<Shape>().Count(s => s.HasImage));

foreach (Shape shape in shapes.OfType<Shape>())
    if (shape.HasImage) 
        shape.Remove();

Assert.AreEqual(0, shapes.OfType<Shape>().Count(s => s.HasImage));
```

Montre comment extraire des images d'un document et les enregistrer sur le système de fichiers local sous forme de fichiers individuels.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Récupérer la collection de formes du document,
// et enregistrez les données d'image de chaque forme avec une image sous forme de fichier sur le système de fichiers local.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
         // Les données d'image des formes peuvent contenir des images de nombreux formats d'image possibles.
        // Nous pouvons déterminer automatiquement une extension de fichier pour chaque image, en fonction de son format.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

### Voir également

* class [Shape](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
