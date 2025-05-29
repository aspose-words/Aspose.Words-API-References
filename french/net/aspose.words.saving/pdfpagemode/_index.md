---
title: PdfPageMode Enum
linktitle: PdfPageMode
articleTitle: PdfPageMode
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.PdfPageMode pour personnaliser l'affichage de vos PDF et améliorer l'expérience utilisateur avec n'importe quel lecteur PDF. Optimisez vos documents dès aujourd'hui !
type: docs
weight: 6300
url: /fr/net/aspose.words.saving/pdfpagemode/
---
## PdfPageMode enumeration

Spécifie comment le document PDF doit être affiché lorsqu'il est ouvert dans le lecteur PDF.

```csharp
public enum PdfPageMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| UseNone | `0` | Ni le plan du document ni les images miniatures ne sont visibles. |
| UseOutlines | `1` | Le plan du document est visible. Notez que s'il n'y a pas de plan dans le document PDF, le volet de navigation du plan ne sera de toute façon pas visible. |
| UseThumbs | `2` | Les images miniatures sont visibles. |
| FullScreen | `3` | Mode plein écran, sans barre de menu, commandes de fenêtre ou toute autre fenêtre visible. |
| UseOC | `4` | Le panneau de groupe de contenu facultatif est visible. |
| UseAttachments | `5` | Le panneau Pièces jointes est visible. |

## Exemples

Montre comment définir les instructions à suivre par certains lecteurs PDF lors de l'ouverture d'un document de sortie.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété « PageMode » sur « PdfPageMode.FullScreen » pour que le lecteur PDF ouvre le fichier enregistré
// document en mode plein écran, qui prend le relais de l'affichage du moniteur et n'a aucun contrôle visible.
// Définissez la propriété « PageMode » sur « PdfPageMode.UseThumbs » pour que le lecteur PDF affiche un panneau séparé
// avec une vignette pour chaque page du document.
// Définissez la propriété « PageMode » sur « PdfPageMode.UseOC » pour que le lecteur PDF affiche un panneau séparé
// qui nous permet de travailler avec n'importe quel calque présent dans le document.
// Définissez la propriété « PageMode » sur « PdfPageMode.UseOutlines » pour obtenir le lecteur PDF
// également pour afficher le contour, si possible.
// Définissez la propriété « PageMode » sur « PdfPageMode.UseNone » pour que le lecteur PDF affiche uniquement le document lui-même.
// Définissez la propriété « PageMode » sur « PdfPageMode.UseAttachments » pour rendre le panneau des pièces jointes visible.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

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
