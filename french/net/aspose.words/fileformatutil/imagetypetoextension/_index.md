---
title: FileFormatUtil.ImageTypeToExtension
linktitle: ImageTypeToExtension
articleTitle: ImageTypeToExtension
second_title: Aspose.Words pour .NET
description: Convertissez facilement les types d'images Aspose.Words en extensions de fichier grâce à la méthode FileFormatUtil. Obtenez des extensions précises en minuscules en quelques secondes !
type: docs
weight: 50
url: /fr/net/aspose.words/fileformatutil/imagetypetoextension/
---
## FileFormatUtil.ImageTypeToExtension method

Convertit une valeur énumérée de type image Aspose.Words en extension de fichier. L'extension renvoyée est une chaîne en minuscules précédée d'un point.

```csharp
public static string ImageTypeToExtension(ImageType imageType)
```

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentException | Lancer quand on ne peut pas convertir. |

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

* enum [ImageType](../../../aspose.words.drawing/imagetype/)
* class [FileFormatUtil](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
