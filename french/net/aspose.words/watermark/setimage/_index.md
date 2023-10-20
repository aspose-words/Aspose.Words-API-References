---
title: Watermark.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words pour .NET
description: Watermark SetImage méthode. Ajoute un filigrane dimage dans le document en C#.
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
| image | Image | Image affichée sous forme de filigrane. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentNullException | Lance lorsque l'image est`nul` . |

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
| image | Image | Image affichée sous forme de filigrane. |
| options | ImageWatermarkOptions | Définit des options supplémentaires pour le filigrane de l'image. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentNullException | Lance lorsque l'image est`nul` . |

## Remarques

Si[`ImageWatermarkOptions`](../../imagewatermarkoptions/) est`nul`, le filigrane sera défini avec les options par défaut.

## Exemples

Montre comment créer un filigrane à partir d’une image dans le système de fichiers local.

```csharp
Document doc = new Document();

            // Modifier l'apparence du filigrane de l'image avec un objet ImageWatermarkOptions,
            // puis transmettez-le en créant un filigrane à partir d'un fichier image.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET48 || JAVA
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);
#elif NET5_0_OR_GREATER || __MOBILE__
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

## SetImage(*string, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_2}

Ajoute un filigrane d'image dans le document.

```csharp
public void SetImage(string imagePath, ImageWatermarkOptions options)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| imagePath | String | Chemin d'accès au fichier image affiché sous forme de filigrane. |
| options | ImageWatermarkOptions | Définit des options supplémentaires pour le filigrane de l'image. |

### Exceptions

| exception | condition |
| --- | --- |
| ArgumentNullException | Lance lorsque le chemin est`nul` . |

## Remarques

Si[`ImageWatermarkOptions`](../../imagewatermarkoptions/) est`nul`, le filigrane sera défini avec les options par défaut.

### Voir également

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
