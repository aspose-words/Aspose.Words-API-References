---
title: ImageData.CropBottom
linktitle: CropBottom
articleTitle: CropBottom
second_title: Aspose.Words pour .NET
description: Découvrez la propriété ImageData CropBottom pour personnaliser facilement vos images en supprimant les parties indésirables du bas pour un ajustement parfait.
type: docs
weight: 60
url: /fr/net/aspose.words.drawing/imagedata/cropbottom/
---
## ImageData.CropBottom property

Définit la fraction de suppression de l'image du côté inférieur.

```csharp
public double CropBottom { get; set; }
```

## Remarques

Le degré de recadrage peut varier de -1,0 à 1,0. La valeur par défaut est 0. Notez qu'une valeur de 1 n'affichera aucune image. Des valeurs négatives entraîneront un rétrécissement de l'image par rapport au bord recadré (l'espace vide entre l'image et le bord recadré sera rempli par la couleur de remplissage de la forme). Des valeurs positives inférieures à 1 entraîneront un étirement de l'image restante pour l'adapter à la forme.

La valeur par défaut est 0.

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
