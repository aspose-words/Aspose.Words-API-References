---
title: OutlineOptions.DefaultBookmarksOutlineLevel
linktitle: DefaultBookmarksOutlineLevel
articleTitle: DefaultBookmarksOutlineLevel
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété DefaultBookmarksOutlineLevel améliore la visibilité des signets dans le plan de vos documents Word. Gagnez en productivité dès aujourd'hui !
type: docs
weight: 50
url: /fr/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

Spécifie le niveau par défaut dans la structure du document auquel afficher les signets Word.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

## Remarques

Le niveau des signets individuels peut être spécifié à l'aide de[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) propriété.

Spécifiez 0 et les signets Word ne seront pas affichés dans le plan du document. Spécifiez 1 et les signets Word seront affichés dans le plan du document au niveau 1 ; 2 pour le niveau 2 et ainsi de suite.

La valeur par défaut est 0. La plage valide est de 0 à 9.

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

* class [OutlineOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
