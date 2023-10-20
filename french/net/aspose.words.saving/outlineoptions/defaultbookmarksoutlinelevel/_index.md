---
title: OutlineOptions.DefaultBookmarksOutlineLevel
linktitle: DefaultBookmarksOutlineLevel
articleTitle: DefaultBookmarksOutlineLevel
second_title: Aspose.Words pour .NET
description: OutlineOptions DefaultBookmarksOutlineLevel propriété. Spécifie le niveau par défaut dans le plan du document auquel afficher les signets Word en C#.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

Spécifie le niveau par défaut dans le plan du document auquel afficher les signets Word.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

## Remarques

Le niveau des signets individuels peut être spécifié en utilisant[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) propriété.

Spécifiez 0 et les signets Word ne seront pas affichés dans le plan du document. Spécifiez 1 et les signets Word seront affichés dans le plan du document au niveau 1 ; 2 pour le niveau 2 et ainsi de suite.

La valeur par défaut est 0. La plage valide est comprise entre 0 et 9.

## Exemples

Montre comment traiter les signets dans les en-têtes/pieds de page d'un document que nous rendons au format PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Définissez la propriété "PageMode" sur "PdfPageMode.UseOutlines" pour afficher le volet de navigation hiérarchique dans le PDF de sortie.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Définit la propriété "DefaultBookmarksOutlineLevel" sur "1" pour afficher tous
// signets au premier niveau du plan dans le PDF de sortie.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// Définissez la propriété "HeaderFooterBookmarksExportMode" sur "HeaderFooterBookmarksExportMode.None" pour
// n'exporte aucun signet situé dans les en-têtes/pieds de page.
// Définissez la propriété "HeaderFooterBookmarksExportMode" sur "HeaderFooterBookmarksExportMode.First" pour
// exporte uniquement les signets dans l'en-tête/pied de page de la première section.
// Définissez la propriété "HeaderFooterBookmarksExportMode" sur "HeaderFooterBookmarksExportMode.All" pour
// exporte les signets qui se trouvent dans tous les en-têtes/pieds de page.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Voir également

* class [OutlineOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
