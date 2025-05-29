---
title: PdfSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words pour .NET
description: Découvrez la propriété de conformité PdfSaveOptions pour garantir que vos documents PDF répondent aux normes de l'industrie en matière de qualité et de compatibilité.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/pdfsaveoptions/compliance/
---
## PdfSaveOptions.Compliance property

Spécifie le niveau de conformité aux normes PDF pour les documents de sortie.

```csharp
public PdfCompliance Compliance { get; set; }
```

## Remarques

La valeur par défaut estPdf17.

## Exemples

Montre comment définir le niveau de conformité aux normes PDF des documents PDF enregistrés.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
// Notez que certaines options PdfSaveOptions sont interdites lors de l'enregistrement selon l'une des normes et automatiquement corrigées.
// Utilisez IWarningCallback pour savoir quelles options sont automatiquement corrigées.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Définissez la propriété « Compliance » sur « PdfCompliance.PdfA1b » pour être conforme à la norme « PDF/A-1b »,
// qui vise à préserver l'apparence visuelle du document pendant qu'Aspose.Words le convertit en PDF.
// Définissez la propriété « Compliance » sur « PdfCompliance.Pdf17 » pour être conforme à la norme « 1.7 ».
// Définissez la propriété « Compliance » sur « PdfCompliance.PdfA1a » pour être conforme à la norme « PDF/A-1a »,
// qui est conforme à la norme « PDF/A-1b » tout en préservant la structure du document d'origine.
// Définissez la propriété « Compliance » sur « PdfCompliance.PdfUa1 » pour être conforme à la norme « PDF/UA-1 » (ISO 14289-1),
// qui vise à définir les documents électroniques représentés en PDF qui permettent de rendre le fichier accessible.
// Définissez la propriété « Compliance » sur « PdfCompliance.Pdf20 » pour être conforme à la norme « PDF 2.0 » (ISO 32000-2).
// Définissez la propriété « Compliance » sur « PdfCompliance.PdfA4 » pour être conforme à la norme « PDF/A-4 » (ISO 19004:2020),
// qui préserve l'apparence visuelle statique du document au fil du temps.
// Définissez la propriété « Compliance » sur « PdfCompliance.PdfA4Ua2 » pour être conforme à la norme PDF/A-4 (ISO 19005-4:2020)
// et les normes PDF/UA-2 (ISO 14289-2:2024).
// Définissez la propriété « Compliance » sur « PdfCompliance.PdfUa2 » pour être conforme à la norme PDF/UA-2 (ISO 14289-2:2024).
// Cela permet de rendre les documents consultables, mais peut augmenter considérablement la taille de documents déjà volumineux.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Voir également

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
