---
title: PdfSaveOptions.CacheBackgroundGraphics
linktitle: CacheBackgroundGraphics
articleTitle: CacheBackgroundGraphics
second_title: Aspose.Words pour .NET
description: PdfSaveOptions CacheBackgroundGraphics propriété. Obtient ou définit une valeur déterminant sil faut ou non mettre en cache les graphiques placés en arrièreplan du document en C#.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/
---
## PdfSaveOptions.CacheBackgroundGraphics property

Obtient ou définit une valeur déterminant s'il faut ou non mettre en cache les graphiques placés en arrière-plan du document.

```csharp
public bool CacheBackgroundGraphics { get; set; }
```

## Remarques

La valeur par défaut est`vrai` et les graphiques d'arrière-plan sont écrits dans le document PDF en tant que xObject.

Lorsque la valeur est`FAUX` les graphiques d’arrière-plan ne sont pas mis en cache.

Certaines formes ne sont pas prises en charge pour la mise en cache (formes avec champs, signets, HRefs).

Le graphique d'arrière-plan du document est constitué de diverses formes, graphiques, images placées dans le pied de page ou l'en-tête, ainsi que l'arrière-plan et la bordure d'une page.

## Exemples

Montre comment mettre en cache les graphiques placés en arrière-plan du document.

```csharp
Document doc = new Document(MyDir + "Background images.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.CacheBackgroundGraphics = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf", saveOptions);

long asposeToPdfSize = new FileInfo(ArtifactsDir + "PdfSaveOptions.CacheBackgroundGraphics.pdf").Length;
long wordToPdfSize = new FileInfo(MyDir + "Background images (word to pdf).pdf").Length;

Assert.Less(asposeToPdfSize, wordToPdfSize);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
