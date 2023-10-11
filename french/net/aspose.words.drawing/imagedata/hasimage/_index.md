---
title: ImageData.HasImage
second_title: Référence de l'API Aspose.Words pour .NET
description: ImageData propriété. Retoursvrai si la forme contient des octets dimage ou lie une image.
type: docs
weight: 110
url: /fr/net/aspose.words.drawing/imagedata/hasimage/
---
## ImageData.HasImage property

Retours`vrai` si la forme contient des octets d'image ou lie une image.

```csharp
public bool HasImage { get; }
```

### Exemples

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
* espace de noms [Aspose.Words.Drawing](../../imagedata/)
* Assemblée [Aspose.Words](../../../)


