---
title: PdfSaveOptions.DisplayDocTitle
linktitle: DisplayDocTitle
articleTitle: DisplayDocTitle
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété DisplayDocTitle de PdfSaveOptions améliore votre expérience PDF en affichant les titres des documents dans la barre de titre Windows pour une identification facile.
type: docs
weight: 90
url: /fr/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

Un indicateur spécifiant si la barre de titre de la fenêtre doit afficher le titre du document tiré de l'entrée Titre du dictionnaire d'informations du document.

```csharp
public bool DisplayDocTitle { get; set; }
```

## Remarques

Si`FAUX`, la barre de titre devrait plutôt afficher le nom du fichier PDF contenant le document.

Ce drapeau est requis par la conformité PDF/UA.`vrai` la valeur sera utilisée automatiquement lors de l'enregistrement de au format PDF/UA.

La valeur par défaut est`FAUX`.

## Exemples

Montre comment afficher le titre du document comme barre de titre.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
// Définissez « DisplayDocTitle » sur « true » pour obtenir certains lecteurs PDF, tels qu'Adobe Acrobat Pro,
// pour afficher la valeur de la propriété intégrée « Titre » du document dans l'onglet qui appartient à ce document.
// Définissez « DisplayDocTitle » sur « false » pour que ces lecteurs affichent le nom de fichier du document.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
