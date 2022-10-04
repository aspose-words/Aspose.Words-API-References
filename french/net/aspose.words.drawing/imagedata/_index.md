---
title: ImageData
second_title: Référence de l'API Aspose.Words pour .NET
description: Définit une image pour une forme.
type: docs
weight: 930
url: /fr/net/aspose.words.drawing/imagedata/
---
## ImageData class

Définit une image pour une forme.

```csharp
public class ImageData
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | Détermine si une image sera affichée en noir et blanc. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | Obtient la collection de bordures de l'image. Les bordures n'ont d'effet que pour les images en ligne. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | Obtient ou définit la luminosité de l'image. La valeur de cette propriété doit être un nombre compris entre 0,0 (le plus sombre) et 1,0 (le plus lumineux). |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | Définit la valeur de couleur de l'image qui sera traitée comme transparente. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | Obtient ou définit le contraste de l'image spécifiée. La valeur de cette propriété doit être un nombre compris entre 0,0 (le moins de contraste) et 1,0 (le plus grand contraste). |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | Définit la fraction de suppression d'image du côté inférieur. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | Définit la fraction de suppression d'image du côté gauche. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | Définit la fraction de suppression d'image du côté droit. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | Définit la fraction de suppression d'image du côté supérieur. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | Détermine si une image s'affichera en mode niveaux de gris. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | Renvoie vrai si la forme contient des octets d'image ou lie une image. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | Obtient ou définit les octets bruts de l'image stockée dans la forme. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | Obtient les informations sur la taille et la résolution de l'image. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | Obtient le type de l'image. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | Renvoie vrai si l'image est liée à la forme (quand[`SourceFullName`](./sourcefullname/) est spécifié). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | Renvoie vrai si l'image est liée et non stockée dans le document. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | Obtient ou définit le chemin et le nom du fichier source de l'image liée. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | Définit le titre d'une image. |

## Méthodes

| Nom | La description |
| --- | --- |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(Stream) | Enregistre l'image dans le flux spécifié. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(string) | Enregistre l'image dans un fichier. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(Image) | Définit l'image que la forme affiche. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(Stream) | Définit l'image que la forme affiche. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(string) | Définit l'image que la forme affiche. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | Renvoie les octets d'image pour n'importe quelle image, que l'image soit stockée ou liée. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | Obtient l'image stockée dans la forme en tant queImage objet. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | Crée et renvoie un flux contenant les octets de l'image. |

### Remarques

Utilisez le[`ImageData`](../shape/imagedata/) propriété pour accéder et modifier l'image à l'intérieur d'une forme. Vous ne créez pas d'instances de la[`ImageData`](./imagedata/) classe directement.

Une image peut être stockée dans une forme, liée à un fichier externe ou les deux (liée et stockée dans le document).

Que l'image soit stockée à l'intérieur de la forme ou liée, vous pouvez toujours accéder à l'image actual à l'aide de la[`ToByteArray`](./tobytearray/) ,[`ToStream`](./tostream/) ,[`ToImage`](./toimage/) ou[`Save`](./save/) methodes. Si l'image est stockée à l'intérieur de la forme, vous pouvez également y accéder directement à l'aide de la[`ImageBytes`](./imagebytes/) propriété.

Pour stocker une image à l'intérieur d'une forme, utilisez la[`SetImage`](./setimage/) méthode. Pour lier une image à une forme, définissez le[`SourceFullName`](./sourcefullname/) propriété.

### Exemples

Montre comment extraire des images d'un document et les enregistrer dans le système de fichiers local en tant que fichiers individuels.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Récupère la collection de formes du document,
// et enregistrez les données d'image de chaque forme avec une image en tant que fichier dans le système de fichiers local.
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

Montre comment insérer une image liée dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Vous trouverez ci-dessous deux manières d'appliquer une image à une forme afin qu'elle puisse l'afficher.
// 1 - Définir la forme pour contenir l'image.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Chaque image que nous stockons dans shape augmentera la taille de notre document.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Définissez la forme à lier à un fichier image dans le système de fichiers local.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// La création de liens vers des images permet d'économiser de l'espace et d'obtenir un document plus petit.
// Cependant, le document ne peut afficher correctement l'image que lorsque
// le fichier image est présent à l'emplacement vers lequel pointe la propriété "SourceFullName" de la forme.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
