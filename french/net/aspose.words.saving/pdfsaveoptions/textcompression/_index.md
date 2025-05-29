---
title: PdfSaveOptions.TextCompression
linktitle: TextCompression
articleTitle: TextCompression
second_title: Aspose.Words pour .NET
description: Découvrez la propriété TextCompression de PdfSaveOptions pour optimiser vos documents. Choisissez le type de compression optimal pour un stockage de texte efficace et un chargement plus rapide.
type: docs
weight: 310
url: /fr/net/aspose.words.saving/pdfsaveoptions/textcompression/
---
## PdfSaveOptions.TextCompression property

Spécifie le type de compression à utiliser pour tout le contenu textuel du document.

```csharp
public PdfTextCompression TextCompression { get; set; }
```

## Remarques

La valeur par défaut estFlate.

Augmente considérablement la taille de sortie lors de l'enregistrement d'un document sans compression.

## Exemples

Montre comment appliquer la compression de texte lors de l'enregistrement d'un document au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définissez la propriété « TextCompression » sur « PdfTextCompression.None » pour ne pas appliquer
// compression en texte lorsque nous enregistrons le document au format PDF.
// Définissez la propriété « TextCompression » sur « PdfTextCompression.Flate » pour appliquer la compression ZIP
// au texte lors de l'enregistrement du document au format PDF. Plus le document est volumineux, plus l'impact sera important.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### Voir également

* enum [PdfTextCompression](../../pdftextcompression/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
