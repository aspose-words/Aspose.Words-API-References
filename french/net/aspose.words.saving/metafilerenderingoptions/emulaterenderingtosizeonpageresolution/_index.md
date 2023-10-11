---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution
second_title: Référence de l'API Aspose.Words pour .NET
description: MetafileRenderingOptions propriété. Obtient ou définit la résolution en pixels par pouce pour lémulation du rendu des métafichiers à la taille de la page.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution property

Obtient ou définit la résolution en pixels par pouce pour l'émulation du rendu des métafichiers à la taille de la page.

```csharp
public int EmulateRenderingToSizeOnPageResolution { get; set; }
```

### Remarques

Cette option est utilisée uniquement lorsque[`EmulateRenderingToSizeOnPage`](../emulaterenderingtosizeonpage/) est réglé sur`vrai`.

La valeur par défaut est 96. Il s'agit d'une résolution d'affichage par défaut. C'est-à-dire que le rendu du métafichier émulera l'affichage de le métafichier dans MS Word avec un facteur de zoom de 100 %.

### Exemples

Montre comment afficher le métafichier en fonction de la taille sur la page.

```csharp
Document doc = new Document(MyDir + "WMF with text.docx");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Définit la propriété "EmulateRenderingToSizeOnPage" sur "true"
// pour émuler le rendu en fonction de la taille du métafichier sur la page.
// Définit la propriété "EmulateRenderingToSizeOnPage" sur "false"
// pour émuler le rendu du métafichier à sa taille par défaut en pixels.
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPage = renderToSize;
saveOptions.MetafileRenderingOptions.EmulateRenderingToSizeOnPageResolution = 50;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmulateRenderingToSizeOnPage.pdf", saveOptions);
```

### Voir également

* class [MetafileRenderingOptions](../)
* espace de noms [Aspose.Words.Saving](../../metafilerenderingoptions/)
* Assemblée [Aspose.Words](../../../)


