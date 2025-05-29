---
title: PageSet Class
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Saving.PageSet pour une gestion efficace des documents. Définissez facilement des ensembles de pages aléatoires et optimisez votre flux de travail dès aujourd'hui !
type: docs
weight: 6170
url: /fr/net/aspose.words.saving/pageset/
---
## PageSet class

Décrit un ensemble aléatoire de pages.

Pour en savoir plus, visitez le[Programmation avec des documents](https://docs.aspose.com/words/net/programming-with-documents/) article de documentation.

```csharp
public sealed class PageSet : IEnumerable<int>
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [PageSet](pageset/#constructor_1)(*int*) | Crée un ensemble d'une page basé sur l'index de page exact. |
| [PageSet](pageset/#constructor_2)(*params int[]*) | Crée un ensemble de pages basé sur des indices de page exacts. |
| [PageSet](pageset/#constructor)(*params PageRange[]*) | Crée un ensemble de pages basé sur des plages. |

## Propriétés

| Nom | La description |
| --- | --- |
| static [All](../../aspose.words.saving/pageset/all/) { get; } | Obtient un ensemble avec toutes les pages du document dans leur ordre d'origine. |
| static [Even](../../aspose.words.saving/pageset/even/) { get; } | Obtient un ensemble avec toutes les pages paires du document dans leur ordre d'origine. |
| static [Odd](../../aspose.words.saving/pageset/odd/) { get; } | Obtient un ensemble avec toutes les pages impaires du document dans leur ordre d'origine. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetEnumerator](../../aspose.words.saving/pageset/getenumerator/)() |  |

## Exemples

Montre comment restituer une page d'un document en une image JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Créez un objet « ImageSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode rend le document en image.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// Définissez le « PageSet » sur « 1 » pour sélectionner la deuxième page via
// l'index de base zéro à partir duquel démarrer le rendu du document.
options.PageSet = new PageSet(1);

// Lorsque nous enregistrons le document au format JPEG, Aspose.Words ne rend qu'une seule page.
// Cette image contiendra une page à partir de la page deux,
// qui sera simplement la deuxième page du document original.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
