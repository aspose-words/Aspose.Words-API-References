---
title: ImageData.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words pour .NET
description: Enregistrez vos images facilement grâce à la méthode ImageData Save. Simplifiez votre flux de travail en stockant vos images directement dans le flux de votre choix, en toute simplicité.
type: docs
weight: 200
url: /fr/net/aspose.words.drawing/imagedata/save/
---
## Save(*Stream*) {#save}

Enregistre l'image dans le flux spécifié.

```csharp
public void Save(Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Le flux dans lequel enregistrer l'image. |

## Remarques

Est-ce la responsabilité de l'appelant de supprimer l'objet de flux ?

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

---

## Save(*string*) {#save_1}

Enregistre l'image dans un fichier.

```csharp
public void Save(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Le nom du fichier où enregistrer l'image. |

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

* class [ImageData](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
