---
title: HeaderFooterBookmarksExportMode Enum
linktitle: HeaderFooterBookmarksExportMode
articleTitle: HeaderFooterBookmarksExportMode
second_title: Aspose.Words pour .NET
description: Aspose.Words.Saving.HeaderFooterBookmarksExportMode énumération. Spécifie comment les signets dans les entêtes/pieds de page sont exportés en C#.
type: docs
weight: 5050
url: /fr/net/aspose.words.saving/headerfooterbookmarksexportmode/
---
## HeaderFooterBookmarksExportMode enumeration

Spécifie comment les signets dans les en-têtes/pieds de page sont exportés.

```csharp
public enum HeaderFooterBookmarksExportMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Les signets dans les en-têtes/pieds de page ne sont pas exportés. |
| First | `1` | Seul le signet du premier en-tête/pied de page de la section est exporté. |
| All | `2` | Les signets de tous les en-têtes/pieds de page sont exportés. |

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
