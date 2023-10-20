---
title: ImageType Enum
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words pour .NET
description: Aspose.Words.Drawing.ImageType énumération. Spécifie le type format dune image dans un document Microsoft Word en C#.
type: docs
weight: 1080
url: /fr/net/aspose.words.drawing/imagetype/
---
## ImageType enumeration

Spécifie le type (format) d'une image dans un document Microsoft Word.

```csharp
public enum ImageType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| NoImage | `0` | Il n'y a pas de données d'image. |
| Unknown | `1` | Un type d'image inconnu ou un type d'image qui ne peut pas être directement stocké dans un document Microsoft Word. |
| Emf | `2` | Métafichier amélioré Windows. |
| Wmf | `3` | Métafichier Windows. |
| Pict | `4` | Macintosh PICT. Une image existante sera conservée dans un document, mais l'insertion de nouvelles images PICT dans un document n'est pas prise en charge. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Graphiques réseau portables. |
| Bmp | `7` | Bitmap Windows. |
| Eps | `8` | PostScript encapsulé. |

## Exemples

Montre comment ajouter une image à une forme et vérifier son type.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");

using (MemoryStream stream = new MemoryStream(imageBytes))
{
    Image image = Image.FromStream(stream);

    // L'image dans l'URL est un .gif. L'insérer dans un document le convertit en .png.
    Shape imgShape = builder.InsertImage(image);
    Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
}
```

### Voir également

* property [ImageType](../imagedata/imagetype/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
