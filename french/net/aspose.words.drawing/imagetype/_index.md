---
title: ImageType Enum
linktitle: ImageType
articleTitle: ImageType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Drawing.ImageType pour gérer facilement les formats d'image dans les documents Microsoft Word. Améliorez l'attrait visuel de vos documents !
type: docs
weight: 1410
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
| Unknown | `1` | Un type d'image inconnu ou un type d'image qui ne peut pas être stocké directement dans un document Microsoft Word. |
| Emf | `2` | Métafichier Windows amélioré. |
| Wmf | `3` | Métafichier Windows. |
| Pict | `4` | Macintosh PICT. Une image existante sera conservée dans un document, mais l'insertion de nouvelles images PICT dans un document n'est pas prise en charge. |
| Jpeg | `5` | JPEG JFIF. |
| Png | `6` | Carte graphique réseau portable. |
| Bmp | `7` | Image bitmap Windows. |
| Eps | `8` | PostScript encapsulé. |
| WebP | `9` | WebP. |
| Gif | `10` | GIF |

## Exemples

Montre comment lire une image WebP.

```csharp
Document doc = new Document(MyDir + "Document with WebP image.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
Assert.AreEqual(ImageType.WebP, shape.ImageData.ImageType);
```

Montre comment ajouter une image à une forme et vérifier son type.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape imgShape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.AreEqual(ImageType.Jpeg, imgShape.ImageData.ImageType);
```

### Voir également

* property [ImageType](../imagedata/imagetype/)
* espace de noms [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Assemblée [Aspose.Words](../../)
