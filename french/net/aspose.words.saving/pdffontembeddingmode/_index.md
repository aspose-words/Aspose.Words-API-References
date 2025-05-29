---
title: PdfFontEmbeddingMode Enum
linktitle: PdfFontEmbeddingMode
articleTitle: PdfFontEmbeddingMode
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.PdfFontEmbeddingMode pour une intégration optimale des polices dans les PDF. Améliorez la qualité de vos documents et assurez un affichage cohérent du texte.
type: docs
weight: 6260
url: /fr/net/aspose.words.saving/pdffontembeddingmode/
---
## PdfFontEmbeddingMode enumeration

Spécifie comment Aspose.Words doit incorporer les polices.

```csharp
public enum PdfFontEmbeddingMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| EmbedAll | `0` | Aspose.Words intègre toutes les polices. |
| EmbedNonstandard | `1` | Aspose.Words intègre toutes les polices à l'exception des polices Windows standard Arial et Times New Roman. Seules les polices Arial et Times New Roman sont affectées dans ce mode car MS Word n'intègre pas uniquement ces polices lors de l'enregistrement du document au format PDF. |
| EmbedNone | `2` | Aspose.Words n'intègre aucune police. |

## Exemples

Montre comment configurer Aspose.Words pour ignorer l'intégration des polices Arial et Times New Roman dans un document PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// "Arial" est une police standard et "Courier New" est une police non standard.
builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Définissez la propriété « EmbedFullFonts » sur « true » pour intégrer chaque glyphe de chaque police intégrée dans le PDF de sortie.
options.EmbedFullFonts = true;
// Définissez la propriété « FontEmbeddingMode » sur « EmbedAll » pour intégrer toutes les polices dans le PDF de sortie.
// Définissez la propriété « FontEmbeddingMode » sur « EmbedNonstandard » pour autoriser uniquement l'incorporation de polices non standard dans le PDF de sortie.
// Définissez la propriété « FontEmbeddingMode » sur « EmbedNone » pour n'intégrer aucune police dans le PDF de sortie.
options.FontEmbeddingMode = pdfFontEmbeddingMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedWindowsFonts.pdf", options);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
