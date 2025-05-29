---
title: ImageData.ImageType
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ImageData ImageType pour identifier facilement les types d'images et améliorer vos capacités de traitement. Optimisez votre efficacité de développement dès aujourd'hui !
type: docs
weight: 140
url: /fr/net/aspose.words.drawing/imagedata/imagetype/
---
## ImageData.ImageType property

Obtient le type de l'image.

```csharp
public ImageType ImageType { get; }
```

## Exemples

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

* enum [ImageType](../../imagetype/)
* class [ImageData](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
