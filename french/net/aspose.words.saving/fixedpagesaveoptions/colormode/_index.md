---
title: FixedPageSaveOptions.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FixedPageSaveOptions ColorMode pour personnaliser le rendu des couleurs et améliorer la qualité et l'esthétique de vos documents. Optimisez vos résultats dès aujourd'hui !
type: docs
weight: 10
url: /fr/net/aspose.words.saving/fixedpagesaveoptions/colormode/
---
## FixedPageSaveOptions.ColorMode property

Obtient ou définit une valeur déterminant la manière dont les couleurs sont rendues.

```csharp
public ColorMode ColorMode { get; set; }
```

## Remarques

La valeur par défaut estNormal .

## Exemples

Montre comment modifier la couleur de l'image avec la propriété des options d'enregistrement.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
// Définissez la propriété « ColorMode » sur « Niveaux de gris » pour rendre toutes les images du document en noir et blanc.
// La taille du document de sortie peut être plus grande avec ce paramètre.
// Définissez la propriété « ColorMode » sur « Normal » pour restituer toutes les images en couleur.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

### Voir également

* enum [ColorMode](../../colormode/)
* class [FixedPageSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
