---
title: ImageData.HasImage
linktitle: HasImage
articleTitle: HasImage
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ImageData HasImage. Vérifiez rapidement si une forme contient des octets d'image ou des liens, améliorant ainsi votre processus de conception sans effort.
type: docs
weight: 110
url: /fr/net/aspose.words.drawing/imagedata/hasimage/
---
## ImageData.HasImage property

Retours`vrai` si la forme contient des octets d'image ou lie une image.

```csharp
public bool HasImage { get; }
```

## Exemples

Montre comment enregistrer toutes les images d'un document dans le système de fichiers.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// Les formes avec l'indicateur « HasImage » défini stockent et affichent toutes les images du document.
Shape[] shapesWithImages = imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>()
    .Where(s => s.HasImage).ToArray();

// Parcourez chaque forme et enregistrez son image.
for (int shapeIndex = 0; shapeIndex < shapesWithImages.Length; ++shapeIndex)
{
    ImageData imageData = shapesWithImages[shapeIndex].ImageData;
    using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{shapeIndex + 1}.{imageData.ImageType}"))
        imageData.Save(fileStream);
}
```

### Voir également

* class [ImageData](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
