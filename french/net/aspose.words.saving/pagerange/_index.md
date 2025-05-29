---
title: PageRange Class
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Saving.PageRange pour définir facilement des plages de pages continues. Améliorez le traitement de vos documents avec précision et efficacité.
type: docs
weight: 6150
url: /fr/net/aspose.words.saving/pagerange/
---
## PageRange class

Représente une plage continue de pages.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article de documentation.

```csharp
public sealed class PageRange
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [PageRange](pagerange/)(*int, int*) | Crée un nouvel objet de plage de pages. |

## Exemples

Montre comment extraire des pages en fonction de plages de pages exactes.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
