---
title: ImageData Class
linktitle: ImageData
articleTitle: ImageData
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Drawing.ImageData : votre solution pour définir et gérer des images dans des formes. Améliorez la conception de vos documents sans effort !
type: docs
weight: 1390
url: /fr/net/aspose.words.drawing/imagedata/
---
## ImageData class

Définit une image pour une forme.

Pour en savoir plus, visitez le[Travailler avec des images](https://docs.aspose.com/words/net/working-with-images/) article de documentation.

```csharp
public class ImageData
```

## Propriétés

| Nom | La description |
| --- | --- |
| [BiLevel](../../aspose.words.drawing/imagedata/bilevel/) { get; set; } | Détermine si une image sera affichée en noir et blanc. |
| [Borders](../../aspose.words.drawing/imagedata/borders/) { get; } | Récupère la collection de bordures de l'image. Les bordures n'ont d'effet que sur les images intégrées. |
| [Brightness](../../aspose.words.drawing/imagedata/brightness/) { get; set; } | Obtient ou définit la luminosité de l'image. La valeur de cette propriété doit être un nombre compris entre 0,0 (le plus faible) et 1,0 (le plus lumineux). |
| [ChromaKey](../../aspose.words.drawing/imagedata/chromakey/) { get; set; } | Définit la valeur de couleur de l'image qui sera traitée comme transparente. |
| [Contrast](../../aspose.words.drawing/imagedata/contrast/) { get; set; } | Récupère ou définit le contraste de l'image spécifiée. La valeur de cette propriété doit être un nombre compris entre 0,0 (contraste le plus faible) et 1,0 (contraste le plus élevé). |
| [CropBottom](../../aspose.words.drawing/imagedata/cropbottom/) { get; set; } | Définit la fraction de suppression de l'image du côté inférieur. |
| [CropLeft](../../aspose.words.drawing/imagedata/cropleft/) { get; set; } | Définit la fraction de suppression d'image du côté gauche. |
| [CropRight](../../aspose.words.drawing/imagedata/cropright/) { get; set; } | Définit la fraction de suppression d'image du côté droit. |
| [CropTop](../../aspose.words.drawing/imagedata/croptop/) { get; set; } | Définit la fraction de suppression de l'image du côté supérieur. |
| [GrayScale](../../aspose.words.drawing/imagedata/grayscale/) { get; set; } | Détermine si une image s'affichera en mode niveaux de gris. |
| [HasImage](../../aspose.words.drawing/imagedata/hasimage/) { get; } | Retours`vrai` si la forme contient des octets d'image ou lie une image. |
| [ImageBytes](../../aspose.words.drawing/imagedata/imagebytes/) { get; set; } | Obtient ou définit les octets bruts de l'image stockée dans la forme. |
| [ImageSize](../../aspose.words.drawing/imagedata/imagesize/) { get; } | Obtient les informations sur la taille et la résolution de l'image. |
| [ImageType](../../aspose.words.drawing/imagedata/imagetype/) { get; } | Obtient le type de l'image. |
| [IsLink](../../aspose.words.drawing/imagedata/islink/) { get; } | Retours`vrai` si l'image est liée à la forme (quand[`SourceFullName`](./sourcefullname/) est spécifié). |
| [IsLinkOnly](../../aspose.words.drawing/imagedata/islinkonly/) { get; } | Retours`vrai` si l'image est liée et non stockée dans le document. |
| [SourceFullName](../../aspose.words.drawing/imagedata/sourcefullname/) { get; set; } | Obtient ou définit le chemin et le nom du fichier source de l'image liée. |
| [Title](../../aspose.words.drawing/imagedata/title/) { get; set; } | Définit le titre d'une image. |

## Méthodes

| Nom | La description |
| --- | --- |
| [FitImageToShape](../../aspose.words.drawing/imagedata/fitimagetoshape/)() | Ajuste les données d'image au cadre de forme afin que le rapport hauteur/largeur des données d'image corresponde au rapport hauteur/largeur du cadre de forme. |
| [Save](../../aspose.words.drawing/imagedata/save/#save)(*Stream*) | Enregistre l'image dans le flux spécifié. |
| [Save](../../aspose.words.drawing/imagedata/save/#save_1)(*string*) | Enregistre l'image dans un fichier. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage)(*Image*) | Définit l'image que la forme affiche. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_1)(*Stream*) | Définit l'image que la forme affiche. |
| [SetImage](../../aspose.words.drawing/imagedata/setimage/#setimage_2)(*string*) | Définit l'image que la forme affiche. |
| [ToByteArray](../../aspose.words.drawing/imagedata/tobytearray/)() | Renvoie les octets d'image pour n'importe quelle image, que l'image soit stockée ou liée. |
| [ToImage](../../aspose.words.drawing/imagedata/toimage/)() | Obtient l'image stockée dans la forme sous forme deImage objet. |
| [ToStream](../../aspose.words.drawing/imagedata/tostream/)() | Crée et renvoie un flux contenant les octets de l'image. |

## Remarques

Utilisez le[`ImageData`](../shape/imagedata/)propriété pour accéder et modifier l'image à l'intérieur d'une forme. Vous ne créez pas d'instances de la`ImageData` classe directement.

Une image peut être stockée dans une forme, liée à un fichier externe ou les deux (liée et stockée dans le document).

Que l'image soit stockée à l'intérieur de la forme ou liée, vous pouvez toujours accéder à l'image actual à l'aide de la[`ToByteArray`](./tobytearray/) ,[`ToStream`](./tostream/) ,[`ToImage`](./toimage/) ou[`Save`](./save/) méthodes. Si l'image est stockée à l'intérieur de la forme, vous pouvez également y accéder directement à l'aide de la[`ImageBytes`](./imagebytes/) propriété.

Pour stocker une image dans une forme, utilisez le[`SetImage`](./setimage/) méthode. Pour lier une image à une forme, définissez la[`SourceFullName`](./sourcefullname/) propriété.

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

Montre comment insérer une image liée dans un document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Vous trouverez ci-dessous deux manières d'appliquer une image à une forme afin qu'elle puisse l'afficher.
// 1 - Définissez la forme pour contenir l'image.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Chaque image que nous stockons dans shape augmentera la taille de notre document.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Définissez la forme pour qu'elle soit liée à un fichier image dans le système de fichiers local.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Lier des images permettra d'économiser de l'espace et d'obtenir un document plus petit.
// Cependant, le document ne peut afficher correctement l'image que pendant
// le fichier image est présent à l'emplacement vers lequel pointe la propriété « SourceFullName » de la forme.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Voir également

* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
