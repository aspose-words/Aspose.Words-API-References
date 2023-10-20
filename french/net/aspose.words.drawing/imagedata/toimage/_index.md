---
title: ImageData.ToImage
linktitle: ToImage
articleTitle: ToImage
second_title: Aspose.Words pour .NET
description: ImageData ToImage méthode. Obtient limage stockée dans la forme en tant queImage objet en C#.
type: docs
weight: 220
url: /fr/net/aspose.words.drawing/imagedata/toimage/
---
## ImageData.ToImage method

Obtient l'image stockée dans la forme en tant queImage objet.

```csharp
public Image ToImage()
```

## Remarques

Un nouveauImage L'objet est créé à chaque fois que cette méthode est appelée.

Il est de la responsabilité de l'appelant de supprimer l'objet image.

## Exemples

Montre comment enregistrer toutes les images d'un document dans le système de fichiers.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");

// Les formes avec le jeu d'indicateurs "HasImage" stockent et affichent toutes les images du document.
IEnumerable<Shape> shapesWithImages = 
    imgSourceDoc.GetChildNodes(NodeType.Shape, true).Cast<Shape>().Where(s => s.HasImage);

// Parcourez chaque forme et enregistrez son image.
ImageFormatConverter formatConverter = new ImageFormatConverter();

using (IEnumerator<Shape> enumerator = shapesWithImages.GetEnumerator())
{
    int shapeIndex = 0;

    while (enumerator.MoveNext())
    {
        ImageData imageData = enumerator.Current.ImageData;
        ImageFormat format = imageData.ToImage().RawFormat;
        string fileExtension = formatConverter.ConvertToString(format);

        using (FileStream fileStream = File.Create(ArtifactsDir + $"Drawing.SaveAllImages.{++shapeIndex}.{fileExtension}"))
            imageData.Save(fileStream);
    }
}
```

### Voir également

* class [ImageData](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
