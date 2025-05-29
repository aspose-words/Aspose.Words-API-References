---
title: PdfSaveOptions.PageLayout
linktitle: PageLayout
articleTitle: PageLayout
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PdfSaveOptions PageLayout pour personnaliser la mise en page de votre PDF et optimiser son affichage dans tous les lecteurs. Améliorez la présentation de votre document !
type: docs
weight: 250
url: /fr/net/aspose.words.saving/pdfsaveoptions/pagelayout/
---
## PdfSaveOptions.PageLayout property

Spécifie la mise en page à utiliser lorsque le document est ouvert dans un lecteur PDF.

```csharp
public PdfPageLayout PageLayout { get; set; }
```

## Remarques

La valeur par défaut estSinglePage .

## Exemples

Montre comment afficher les pages lorsqu'elles sont ouvertes dans un lecteur PDF.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Affichez les pages deux par deux, avec les pages impaires à gauche.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### Voir également

* enum [PdfPageLayout](../../pdfpagelayout/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
