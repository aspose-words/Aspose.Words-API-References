---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: Aspose.Words pour .NET
description: SaveOptions MemoryOptimization propriété. Obtient ou définit la valeur déterminant si loptimisation de la mémoire doit être effectuée avant denregistrer le document. La valeur par défaut de cette propriété estFAUX  en C#.
type: docs
weight: 100
url: /fr/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

Obtient ou définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est`FAUX` .

```csharp
public bool MemoryOptimization { get; set; }
```

## Remarques

Définir cette option sur`vrai` peut réduire considérablement la consommation de mémoire tout en enregistrant des documents volumineux au prix d'un temps d'enregistrement plus lent.

## Exemples

Affiche une option pour optimiser la consommation de mémoire lors du rendu de documents volumineux au format PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Définissez la propriété "MemoryOptimization" sur "true" pour réduire l'empreinte mémoire des opérations de sauvegarde des documents volumineux
// au prix d'une augmentation de la durée de l'opération.
// Définissez la propriété "MemoryOptimization" sur "false" pour enregistrer normalement le document au format PDF.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
