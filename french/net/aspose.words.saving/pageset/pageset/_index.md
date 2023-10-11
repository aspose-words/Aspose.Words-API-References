---
title: PageSet.PageSet
second_title: Référence de l'API Aspose.Words pour .NET
description: PageSet constructeur. Crée un ensemble dune page basé sur lindex exact de la page.
type: docs
weight: 10
url: /fr/net/aspose.words.saving/pageset/pageset/
---
## PageSet(int) {#constructor_1}

Crée un ensemble d'une page basé sur l'index exact de la page.

```csharp
public PageSet(int page)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| page | Int32 | Index de base zéro de la page. |

### Remarques

Si une page rencontrée ne figure pas dans le document, une exception sera levée lors du rendu. MaxValue signifie la dernière page du document.

### Voir également

* class [PageSet](../)
* espace de noms [Aspose.Words.Saving](../../pageset/)
* Assemblée [Aspose.Words](../../../)

---

## PageSet(params int[]) {#constructor_2}

Crée un ensemble de pages basé sur des index de page exacts.

```csharp
public PageSet(params int[] pages)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| pages | Int32[] | Index des pages de base zéro. |

### Remarques

Si une page rencontrée ne figure pas dans le document, une exception sera levée lors du rendu. MaxValue signifie la dernière page du document.

### Exemples

Montre comment extraire des pages en fonction d'index de page exacts.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ajoute cinq pages au document.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Crée un objet "XpsSaveOptions", que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Utilisez la propriété "PageSet" pour sélectionner un ensemble de pages du document à enregistrer dans la sortie XPS.
// Dans ce cas, nous choisirons, via un index de base zéro, seulement trois pages : page 1, page 2 et page 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### Voir également

* class [PageSet](../)
* espace de noms [Aspose.Words.Saving](../../pageset/)
* Assemblée [Aspose.Words](../../../)

---

## PageSet(params PageRange[]) {#constructor}

Crée un ensemble de pages basé sur des plages.

```csharp
public PageSet(params PageRange[] ranges)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| ranges | PageRange[] | Tableau de plages de pages. |

### Remarques

Si une plage commence après la dernière page du document, une exception sera levée lors du rendu. Toutes les plages qui se terminent après la dernière page sont tronquées pour tenir dans le document.

### Exemples

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
* espace de noms [Aspose.Words.Saving](../../pageset/)
* Assemblée [Aspose.Words](../../../)


