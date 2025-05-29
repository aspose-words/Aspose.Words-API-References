---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: Aspose.Words pour .NET
description: Améliorez les performances de vos documents grâce à la propriété SaveOptions MemoryOptimization. Contrôlez l'utilisation de la mémoire avant l'enregistrement, pour plus d'efficacité et de rapidité.
type: docs
weight: 100
url: /fr/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

Obtient ou définit une valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est`FAUX` .

```csharp
public bool MemoryOptimization { get; set; }
```

## Remarques

Définition de cette option sur`vrai` peut réduire considérablement la consommation de mémoire tout en enregistrant des documents volumineux au prix d'un temps d'enregistrement plus lent.

## Exemples

Affiche une option pour optimiser la consommation de mémoire lors du rendu de documents volumineux au format PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Définissez la propriété « MemoryOptimization » sur « true » pour réduire l'empreinte mémoire des opérations de sauvegarde de documents volumineux
// au prix d'une augmentation de la durée de l'opération.
// Définissez la propriété « MemoryOptimization » sur « false » pour enregistrer normalement le document au format PDF.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
