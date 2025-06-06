---
title: PageRange
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words pour .NET
description: Créez facilement des plages de pages personnalisées grâce à notre constructeur de plages de pages. Optimisez la gestion de vos documents avec précision et flexibilité.
type: docs
weight: 10
url: /fr/net/aspose.words.saving/pagerange/pagerange/
---
## PageRange constructor

Crée un nouvel objet de plage de pages.

```csharp
public PageRange(int from, int to)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| from | Int32 | L'index de base zéro de la page de départ. |
| to | Int32 | L'index de base zéro de la page de fin. S'il dépasse l'index de la dernière page du document, il est tronqué pour tenir dans le document lors du rendu. |

## Remarques

MaxValue signifie la dernière page du document.

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

* class [PageRange](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
