---
title: MetafileRenderingOptions.EmulateRenderingToSizeOnPage
linktitle: EmulateRenderingToSizeOnPage
articleTitle: EmulateRenderingToSizeOnPage
second_title: Aspose.Words pour .NET
description: MetafileRenderingOptions EmulateRenderingToSizeOnPage propriété. Obtient ou définit une valeur déterminant si le rendu du métafichier émule laffichage du métafichier en fonction de la taille sur la page ou laffichage du métafichier dans sa taille par défaut en C#.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/
---
## MetafileRenderingOptions.EmulateRenderingToSizeOnPage property

Obtient ou définit une valeur déterminant si le rendu du métafichier émule l'affichage du métafichier en fonction de la taille sur la page ou l'affichage du métafichier dans sa taille par défaut.

```csharp
public bool EmulateRenderingToSizeOnPage { get; set; }
```

## Remarques

Lorsque les métafichiers sont affichés dans MS Word, certains graphiques peuvent être mis à l'échelle en fonction de la taille réelle du métafichier en pixels. C'est-à-dire que même le zoom peut affecter l'affichage du métafichier.

Lorsque cette valeur est fixée à`vrai` Aspose.Words émule le rendu en fonction de la taille du métafichier sur la page. La taille en pixels est calculée à partir de la taille du métafichier sur la page et de la valeur spécifiée.[`EmulateRenderingToSizeOnPageResolution`](../emulaterenderingtosizeonpageresolution/).

Lorsque cette valeur est fixée à`FAUX`, Aspose.Words émule le rendu des métafichiers à sa taille par défaut en pixels.

Cette option est utilisée uniquement lorsque le métafichier est rendu sous forme de graphiques vectoriels.

La valeur par défaut est`vrai`.

## Exemples

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
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
