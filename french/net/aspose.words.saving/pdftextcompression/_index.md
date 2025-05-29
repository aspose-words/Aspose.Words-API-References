---
title: PdfTextCompression Enum
linktitle: PdfTextCompression
articleTitle: PdfTextCompression
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.PdfTextCompression pour une compression efficace du contenu PDF, améliorant la taille et les performances des fichiers tout en préservant la qualité.
type: docs
weight: 6330
url: /fr/net/aspose.words.saving/pdftextcompression/
---
## PdfTextCompression enumeration

Spécifie un type de compression appliqué à tout le contenu du fichier PDF, à l'exception des images.

```csharp
public enum PdfTextCompression
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Aucune compression. |
| Flate | `1` | Compression Flate (ZIP). |

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

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
