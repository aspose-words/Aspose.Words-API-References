---
title: PdfTextCompression Enum
linktitle: PdfTextCompression
articleTitle: PdfTextCompression
second_title: Aspose.Words pour .NET
description: Aspose.Words.Saving.PdfTextCompression énumération. Spécifie un type de compression appliqué à tout le contenu du fichier PDF à lexception des images en C#.
type: docs
weight: 5530
url: /fr/net/aspose.words.saving/pdftextcompression/
---
## PdfTextCompression enumeration

Spécifie un type de compression appliqué à tout le contenu du fichier PDF à l'exception des images.

```csharp
public enum PdfTextCompression
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` | Aucune compression. |
| Flate | `1` | Compression plate (ZIP). |

## Exemples

Montre comment appliquer une compression de texte lors de l'enregistrement d'un document au format PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Définit la propriété "TextCompression" sur "PdfTextCompression.None" pour n'appliquer aucune
// compression en texte lorsque nous enregistrons le document au format PDF.
// Définissez la propriété "TextCompression" sur "PdfTextCompression.Flate" pour appliquer la compression ZIP
// en texte lorsque nous enregistrons le document au format PDF. Plus le document est volumineux, plus l’impact qu’il aura sera important.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
