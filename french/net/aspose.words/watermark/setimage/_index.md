---
title: Watermark.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words pour .NET
description: Sublimez vos documents avec la méthode Watermark SetImage. Ajoutez facilement de superbes filigranes d'image pour une touche professionnelle.
type: docs
weight: 30
url: /fr/net/aspose.words/watermark/setimage/
---
## SetImage(*Image*) {#setimage}

Ajoute un filigrane d'image dans le document.

```csharp
public void SetImage(Image image)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| image | Image | Image affichée en filigrane. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentNullException | Lancé lorsque l'image est`nul` . |

## Exemples

Montre comment créer un filigrane à partir d'une image dans le système de fichiers local.

```csharp
Document doc = new Document();

            // Modifiez l'apparence du filigrane de l'image avec un objet ImageWatermarkOptions,
            // puis transmettez-le lors de la création d'un filigrane à partir d'un fichier image.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Nous avons différentes options pour insérer une image :
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Voir également

* class [Watermark](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(*Image, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_1}

Ajoute un filigrane d'image dans le document.

```csharp
public void SetImage(Image image, ImageWatermarkOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| image | Image | Image affichée en filigrane. |
| options | ImageWatermarkOptions | Définit des options supplémentaires pour le filigrane de l'image. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentNullException | Lancé lorsque l'image est`nul` . |

## Remarques

Si[`ImageWatermarkOptions`](../../imagewatermarkoptions/) est`nul`, le filigrane sera défini avec les options par défaut.

## Exemples

Montre comment créer un filigrane à partir d'une image dans le système de fichiers local.

```csharp
Document doc = new Document();

            // Modifiez l'apparence du filigrane de l'image avec un objet ImageWatermarkOptions,
            // puis transmettez-le lors de la création d'un filigrane à partir d'un fichier image.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Nous avons différentes options pour insérer une image :
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Voir également

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(*string, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_3}

Ajoute un filigrane d'image dans le document.

```csharp
public void SetImage(string imagePath, ImageWatermarkOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| imagePath | String | Chemin vers le fichier image qui s'affiche sous forme de filigrane. |
| options | ImageWatermarkOptions | Définit des options supplémentaires pour le filigrane de l'image. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentNullException | Lancé lorsque le chemin est`nul` . |

## Remarques

Si[`ImageWatermarkOptions`](../../imagewatermarkoptions/) est`nul`, le filigrane sera défini avec les options par défaut.

## Exemples

Montre comment créer un filigrane à partir d'une image dans le système de fichiers local.

```csharp
Document doc = new Document();

            // Modifiez l'apparence du filigrane de l'image avec un objet ImageWatermarkOptions,
            // puis transmettez-le lors de la création d'un filigrane à partir d'un fichier image.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Nous avons différentes options pour insérer une image :
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Voir également

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)

---

## SetImage(*Stream, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_2}

Ajoute un filigrane d'image dans le document.

```csharp
public void SetImage(Stream imageStream, ImageWatermarkOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| imageStream | Stream | Le flux contenant les données d'image affichées sous forme de filigrane. |
| options | ImageWatermarkOptions | Définit des options supplémentaires pour le filigrane de l'image. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentNullException | Lancé lorsque le chemin est`nul` . |

## Remarques

Si[`ImageWatermarkOptions`](../../imagewatermarkoptions/) est`nul`, le filigrane sera défini avec les options par défaut.

## Exemples

Montre comment créer un filigrane à partir d'un flux d'images.

```csharp
Document doc = new Document();

// Modifiez l'apparence du filigrane de l'image avec un objet ImageWatermarkOptions,
// puis transmettez-le lors de la création d'un filigrane à partir d'un fichier image.
ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
imageWatermarkOptions.Scale = 5;

using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
    doc.Watermark.SetImage(imageStream, imageWatermarkOptions);

doc.Save(ArtifactsDir + "Document.ImageWatermarkStream.docx");
```

### Voir également

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
