---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
linktitle: EmulateRenderingToSizeOnPageResolution
articleTitle: EmulateRenderingToSizeOnPageResolution
second_title: Aspose.Words pour .NET
description: Découvrez la propriété MetafileRenderingOptions EmulateRenderingToSizeOnPageResolution. Contrôlez la résolution de rendu des métafichiers pour un affichage optimal des pages.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

Obtient ou définit la résolution en pixels par pouce pour l'émulation du rendu du métafichier à la taille de la page.

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

## Remarques

Cette option est utilisée uniquement lorsque[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/) est réglé sur`vrai`.

La valeur par défaut est 96. Il s'agit de la résolution d'affichage par défaut. Autrement dit, le rendu du métafichier simulera l'affichage du métafichier dans MS Word avec un facteur de zoom de 100 %.

## Exemples

Montre comment afficher le métafichier en fonction de la taille sur la page.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Définissez la propriété « EmulateRenderingToSizeOnPage » sur « true »
// pour émuler le rendu en fonction de la taille du métafichier sur la page.
// Définissez la propriété « EmulateRenderingToSizeOnPage » sur « false »
// pour émuler le rendu du métafichier à sa taille par défaut en pixels.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Voir également

* class [MetafileRenderingOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
