---
title: ImageData.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words pour .NET
description: Découvrez comment utiliser la méthode SetImage dans ImageData pour enrichir vos formes avec des images personnalisées. Sublimez votre design sans effort !
type: docs
weight: 210
url: /fr/net/aspose.words.drawing/imagedata/setimage/
---
## SetImage(*Image*) {#setimage}

Définit l'image que la forme affiche.

```csharp
public void SetImage(Image image)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| image | Image | L'objet image. |

## Exemples

Montre comment afficher des images du système de fichiers local dans un document.

```csharp
Document doc = new Document();

// Pour afficher une image dans un document, nous devrons créer une forme
// qui contiendra une image, puis l'ajoutera au corps du document.
Shape imgShape;

// Vous trouverez ci-dessous deux manières d'obtenir une image à partir d'un fichier du système de fichiers local.
// 1 - Créer un objet image à partir d'un fichier image :
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - Ouvrir un fichier image à partir du système de fichiers local à l'aide d'un flux :
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### Voir également

* class [ImageData](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(*Stream*) {#setimage_1}

Définit l'image que la forme affiche.

```csharp
public void SetImage(Stream stream)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| stream | Stream | Le flux qui contient l'image. |

## Exemples

Montre comment afficher des images du système de fichiers local dans un document.

```csharp
Document doc = new Document();

// Pour afficher une image dans un document, nous devrons créer une forme
// qui contiendra une image, puis l'ajoutera au corps du document.
Shape imgShape;

// Vous trouverez ci-dessous deux manières d'obtenir une image à partir d'un fichier du système de fichiers local.
// 1 - Créer un objet image à partir d'un fichier image :
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - Ouvrir un fichier image à partir du système de fichiers local à l'aide d'un flux :
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### Voir également

* class [ImageData](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(*string*) {#setimage_2}

Définit l'image que la forme affiche.

```csharp
public void SetImage(string fileName)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| fileName | String | Le fichier image. Il peut s'agir d'un nom de fichier ou d'une URL. |

## Exemples

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

* class [ImageData](../)
* espace de noms [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../../)
