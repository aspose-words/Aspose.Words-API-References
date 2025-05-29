---
title: PdfSaveOptions.FontEmbeddingMode
linktitle: FontEmbeddingMode
articleTitle: FontEmbeddingMode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FontEmbeddingMode de PdfSaveOptions pour optimiser l'incorporation des polices de vos PDF. Améliorez la qualité et la compatibilité de vos documents sans effort !
type: docs
weight: 170
url: /fr/net/aspose.words.saving/pdfsaveoptions/fontembeddingmode/
---
## PdfSaveOptions.FontEmbeddingMode property

Spécifie le mode d'incorporation de la police.

```csharp
public PdfFontEmbeddingMode FontEmbeddingMode { get; set; }
```

## Remarques

La valeur par défaut estEmbedAll.

Ce paramètre ne fonctionne que pour le texte au format ANSI (Windows-1252). Si le document contient du texte non ANSI, les polices correspondantes seront intégrées, quel que soit le paramètre.

La conformité PDF/A et PDF/UA exige que toutes les polices soient intégrées. EmbedAll la valeur sera utilisée automatiquement lors de l'enregistrement dans PDF/A et PDF/UA.

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

* enum [PdfFontEmbeddingMode](../../pdffontembeddingmode/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
