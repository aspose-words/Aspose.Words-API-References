---
title: PdfSaveOptions.PageMode
linktitle: PageMode
articleTitle: PageMode
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété PdfSaveOptions PageMode améliore votre expérience de visualisation PDF en personnalisant l'affichage des documents dans n'importe quel lecteur PDF.
type: docs
weight: 260
url: /fr/net/aspose.words.saving/pdfsaveoptions/pagemode/
---
## PdfSaveOptions.PageMode property

Spécifie comment le document PDF doit être affiché lorsqu'il est ouvert dans un lecteur PDF.

```csharp
public PdfPageMode PageMode { get; set; }
```

## Remarques

La valeur par défaut estUseOutlines .

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

* enum [PdfPageMode](../../pdfpagemode/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
