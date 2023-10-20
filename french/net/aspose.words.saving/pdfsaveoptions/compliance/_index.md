---
title: PdfSaveOptions.Compliance
linktitle: Compliance
articleTitle: Compliance
second_title: Aspose.Words pour .NET
description: PdfSaveOptions Compliance propriété. Spécifie le niveau de conformité aux normes PDF pour les documents de sortie en C#.
type: docs
weight: 40
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

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
// Notez que certaines PdfSaveOptions sont interdites lors de l'enregistrement dans l'un des standards et automatiquement corrigées.
// Utilisez IWarningCallback pour savoir quelles options sont automatiquement corrigées.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Fixer la propriété "Compliance" à "PdfCompliance.PdfA1b" pour être conforme à la norme "PDF/A-1b",
// qui vise à préserver l'apparence visuelle du document au fur et à mesure qu'Aspose.Words le convertit en PDF.
// Définissez la propriété "Compliance" sur "PdfCompliance.Pdf17" pour être conforme à la norme "1.7".
// Fixer la propriété "Compliance" à "PdfCompliance.PdfA1a" pour être conforme à la norme "PDF/A-1a",
// qui est conforme à "PDF/A-1b" tout en préservant la structure du document original.
// Fixer la propriété "Compliance" à "PdfCompliance.PdfUa1" pour être conforme à la norme "PDF/UA-1" (ISO 14289-1),
// qui vise à définir des documents électroniques représentatifs en PDF qui permettent au fichier d'être accessible.
// Définissez la propriété "Compliance" sur "PdfCompliance.Pdf20" pour être conforme à la norme "PDF 2.0" (ISO 32000-2).
// Définissez la propriété "Compliance" sur "PdfCompliance.PdfA4" pour être conforme à la norme "PDF/A-4" (ISO 19004:2020),
// qui préserve l'apparence visuelle statique du document au fil du temps.
// Cela facilite la recherche dans les documents mais peut augmenter considérablement la taille de documents déjà volumineux.
saveOptions.Compliance = pdfCompliance;

doc.Save(ArtifactsDir + "PdfSaveOptions.Compliance.pdf", saveOptions);
```

### Voir également

* enum [PdfCompliance](../../pdfcompliance/)
* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
