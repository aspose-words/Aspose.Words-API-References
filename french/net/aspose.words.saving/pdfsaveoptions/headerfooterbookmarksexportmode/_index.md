---
title: PdfSaveOptions.HeaderFooterBookmarksExportMode
linktitle: HeaderFooterBookmarksExportMode
articleTitle: HeaderFooterBookmarksExportMode
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété HeaderFooterBookmarksExportMode de PdfSaveOptions optimise l'exportation des signets dans les en-têtes et les pieds de page pour des fonctionnalités PDF améliorées.
type: docs
weight: 180
url: /fr/net/aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/
---
## PdfSaveOptions.HeaderFooterBookmarksExportMode property

Détermine comment les signets dans les en-têtes/pieds de page sont exportés.

```csharp
public HeaderFooterBookmarksExportMode HeaderFooterBookmarksExportMode { get; set; }
```

## Remarques

La valeur par défaut estAll.

Cette propriété est utilisée en conjonction avec le[`OutlineOptions`](../outlineoptions/) option.

## Exemples

Montre comment traiter les signets dans les en-têtes/pieds de page d'un document que nous rendons au format PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Définissez la propriété « PageMode » sur « PdfPageMode.UseOutlines » pour afficher le volet de navigation du plan dans le PDF de sortie.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Définissez la propriété « DefaultBookmarksOutlineLevel » sur « 1 » pour tout afficher
// signets au premier niveau du plan dans le PDF de sortie.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Définissez la propriété « HeaderFooterBookmarksExportMode » sur « HeaderFooterBookmarksExportMode.None » pour
// n'exportez aucun signet qui se trouve à l'intérieur des en-têtes/pieds de page.
// Définissez la propriété « HeaderFooterBookmarksExportMode » sur « HeaderFooterBookmarksExportMode.First » pour
// exporter uniquement les signets dans l'en-tête/les pieds de page de la première section.
// Définissez la propriété « HeaderFooterBookmarksExportMode » sur « HeaderFooterBookmarksExportMode.All » pour
// exporter les signets qui se trouvent dans tous les en-têtes/pieds de page.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Voir également

* enum [HeaderFooterBookmarksExportMode](../../headerfooterbookmarksexportmode/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
