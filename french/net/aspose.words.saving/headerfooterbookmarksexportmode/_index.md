---
title: HeaderFooterBookmarksExportMode Enum
linktitle: HeaderFooterBookmarksExportMode
articleTitle: HeaderFooterBookmarksExportMode
second_title: Aspose.Words pour .NET
description: Découvrez comment Aspose.Words.Saving.HeaderFooterBookmarksExportMode améliore l'exportation des signets dans les en-têtes et les pieds de page pour une gestion transparente des documents.
type: docs
weight: 5800
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
| First | `1` | Seul le signet dans le premier en-tête/pied de page de la section est exporté. |
| All | `2` | Les signets dans tous les en-têtes/pieds de page sont exportés. |

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
