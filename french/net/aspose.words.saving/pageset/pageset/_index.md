---
title: PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words pour .NET
description: Créez sans effort un ensemble de pages personnalisé avec le constructeur PageSet, conçu pour une indexation de page précise et une expérience utilisateur transparente.
type: docs
weight: 10
url: /fr/net/aspose.words.saving/pageset/pageset/
---
## PageSet(*int*) {#constructor_1}

Crée un ensemble d'une page basé sur l'index de page exact.

```csharp
public PageSet(int page)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| page | Int32 | Index de base zéro de la page. |

## Remarques

Si une page est rencontrée qui n'est pas dans le document, une exception sera levée lors du rendu. MaxValue signifie la dernière page du document.

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

* class [PageSet](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)

---

## PageSet(*params int[]*) {#constructor_2}

Crée un ensemble de pages basé sur des indices de page exacts.

```csharp
public PageSet(params int[] pages)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| pages | Int32[] | Index de pages à partir de zéro. |

## Remarques

Si une page est rencontrée qui n'est pas dans le document, une exception sera levée lors du rendu. MaxValue signifie la dernière page du document.

## Exemples

Montre comment extraire des pages en fonction d'index de page exacts.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoutez cinq pages au document.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Créez un objet « XpsSaveOptions », que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Utilisez la propriété « PageSet » pour sélectionner un ensemble de pages du document à enregistrer dans la sortie XPS.
// Dans ce cas, nous choisirons, via un index de base zéro, seulement trois pages : page 1, page 2 et page 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### Voir également

* class [PageSet](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)

---

## PageSet(*params PageRange[]*) {#constructor}

Crée un ensemble de pages basé sur des plages.

```csharp
public PageSet(params PageRange[] ranges)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| ranges | PageRange[] | Tableau de plages de pages. |

## Remarques

Si une plage est rencontrée qui commence après la dernière page du document, une exception sera levée lors du rendu. Toutes les plages qui se terminent après la dernière page sont tronquées pour tenir dans le document.

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

* class [PageRange](../../pagerange/)
* class [PageSet](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
