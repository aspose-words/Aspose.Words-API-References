---
title: ImageData.Borders
linktitle: Borders
articleTitle: Borders
second_title: Aspose.Words pour .NET
description: ImageData Borders propriété. Obtient la collection de bordures de limage. Les bordures nont deffet que sur les images en ligne en C#.
type: docs
weight: 20
url: /fr/net/aspose.words.drawing/imagedata/borders/
---
## ImageData.Borders property

Obtient la collection de bordures de l'image. Les bordures n'ont d'effet que sur les images en ligne.

```csharp
public BorderCollection Borders { get; }
```

## Exemples

Montre comment modifier les données d’image d’une forme.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// Importez une forme depuis le document source et ajoutez-la au premier paragraphe.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// La forme importée contient une image. Nous pouvons accéder aux propriétés et aux données brutes de l'image via l'objet ImageData.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// Si une image n'a pas de bordures, son objet ImageData définira la couleur de la bordure comme vide.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// Cette image n'est pas liée à une autre forme ou fichier image dans le système de fichiers local.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// Les propriétés "Luminosité" et "Contraste" définissent la luminosité et le contraste de l'image
// sur une échelle de 0 à 1, avec la valeur par défaut à 0,5.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// Les valeurs de luminosité et de contraste ci-dessus ont créé une image avec beaucoup de blanc.
// Nous pouvons sélectionner une couleur avec la propriété ChromaKey à remplacer par de la transparence, comme le blanc.
imageData.ChromaKey = Color.White;

// Importez à nouveau la forme source et définissez l'image en monochrome.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// Importez à nouveau la forme source pour créer une troisième image et définissez-la sur BiLevel.
// BiLevel définit chaque pixel en noir ou en blanc, selon la couleur la plus proche de la couleur d'origine.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// Le recadrage est déterminé sur une échelle de 0 à 1. Recadrer un côté de 0,3
// recadrera 30 % de l'image sur le côté recadré.
importedShape.ImageData.CropBottom = 0.3;
importedShape.ImageData.CropLeft = 0.3;
importedShape.ImageData.CropTop = 0.3;
importedShape.ImageData.CropRight = 0.3;

dstDoc.Save(ArtifactsDir + "Drawing.ImageData.docx");
```

### Voir également

* class [BorderCollection](../../../aspose.words/bordercollection/)
* class [ImageData](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
