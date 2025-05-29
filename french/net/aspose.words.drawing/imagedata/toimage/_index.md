---
title: ImageData.ToImage
linktitle: ToImage
articleTitle: ToImage
second_title: Aspose.Words pour .NET
description: Exploitez la puissance de la méthode ToImage dans ImageData pour récupérer facilement les images stockées dans des formes sous forme d'objets Image. Optimisez vos projets sans effort !
type: docs
weight: 230
url: /fr/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

Obtient l'image stockée dans la forme sous forme deImage objet.

```csharp
public Image ToImage()
```

## Remarques

Un nouveauImage l'objet est créé à chaque fois que cette méthode est appelée.

Il est de la responsabilité de l'appelant de disposer de l'objet image.

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
