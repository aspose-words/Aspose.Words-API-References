---
title: ImageData.Brightness
linktitle: Brightness
articleTitle: Brightness
second_title: Aspose.Words pour .NET
description: Ajustez la luminosité de votre image avec la propriété Luminosité d'ImageData. Définissez des valeurs de 0,0 (intensité minimale) à 1,0 (luminosité maximale) pour un impact visuel optimal.
type: docs
weight: 30
url: /fr/net/aspose.words.drawing/imagedata/brightness/
---
## ImageData.Brightness property

Obtient ou définit la luminosité de l'image. La valeur de cette propriété doit être un nombre compris entre 0,0 (le plus faible) et 1,0 (le plus lumineux).

```csharp
public double Brightness { get; set; }
```

## Remarques

La valeur par défaut est 0,5.

## Exemples

Montre comment modifier les données d'image d'une forme.

```csharp
Document imgSourceDoc = new Document(MyDir + "Images.docx");
Shape sourceShape = (Shape)imgSourceDoc.GetChildNodes(NodeType.Shape, true)[0];

Document dstDoc = new Document();

// Importez une forme à partir du document source et ajoutez-la au premier paragraphe.
Shape importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

// La forme importée contient une image. Nous pouvons accéder aux propriétés et aux données brutes de l'image via l'objet ImageData.
ImageData imageData = importedShape.ImageData;
imageData.Title = "Imported Image";

Assert.True(imageData.HasImage);

// Si une image n'a pas de bordures, son objet ImageData définira la couleur de la bordure comme vide.
Assert.AreEqual(4, imageData.Borders.Count);
Assert.AreEqual(Color.Empty, imageData.Borders[0].Color);

// Cette image n'est pas liée à un autre fichier de forme ou d'image dans le système de fichiers local.
Assert.False(imageData.IsLink);
Assert.False(imageData.IsLinkOnly);

// Les propriétés « Luminosité » et « Contraste » définissent la luminosité et le contraste de l'image
// sur une échelle de 0 à 1, avec la valeur par défaut à 0,5.
imageData.Brightness = 0.8;
imageData.Contrast = 1.0;

// Les valeurs de luminosité et de contraste ci-dessus ont créé une image avec beaucoup de blanc.
// Nous pouvons sélectionner une couleur avec la propriété ChromaKey pour la remplacer par la transparence, comme le blanc.
imageData.ChromaKey = Color.White;

// Importez à nouveau la forme source et définissez l'image sur monochrome.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.GrayScale = true;

// Importez à nouveau la forme source pour créer une troisième image et définissez-la sur BiLevel.
// BiLevel définit chaque pixel sur noir ou blanc, selon la couleur la plus proche de la couleur d'origine.
importedShape = (Shape)dstDoc.ImportNode(sourceShape, true);
dstDoc.FirstSection.Body.FirstParagraph.AppendChild(importedShape);

importedShape.ImageData.BiLevel = true;

// Le recadrage est déterminé sur une échelle de 0 à 1. Recadrage d'un côté par 0,3
// recadrera 30 % de l'image sur le côté recadré.
importedShape.ImageData.CropBottom = 0.3;
importedShape.ImageData.CropLeft = 0.3;
importedShape.ImageData.CropTop = 0.3;
importedShape.ImageData.CropRight = 0.3;

dstDoc.Save(ArtifactsDir + "Drawing.ImageData.docx");
```

### Voir également

* class [ImageData](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
