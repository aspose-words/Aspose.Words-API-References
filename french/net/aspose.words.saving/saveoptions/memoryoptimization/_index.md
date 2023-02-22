---
title: SaveOptions.MemoryOptimization
second_title: Référence de l'API Aspose.Words pour .NET
description: SaveOptions propriété. Obtient ou définit la valeur déterminant si loptimisation de la mémoire doit être effectuée avant denregistrer le document. La valeur par défaut de cette propriété est faux .
type: docs
weight: 110
url: /fr/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

Obtient ou définit la valeur déterminant si l'optimisation de la mémoire doit être effectuée avant d'enregistrer le document. La valeur par défaut de cette propriété est **faux** .

```csharp
public bool MemoryOptimization { get; set; }
```

### Remarques

La définition de cette option sur true peut réduire considérablement la consommation de mémoire lors de l'enregistrement de documents volumineux au prix d'un gain de temps plus lent.

### Exemples

Affiche une option pour optimiser la consommation de mémoire lors du rendu de documents volumineux au format PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crée un objet "PdfSaveOptions" que nous pouvons passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Définissez la propriété "MemoryOptimization" sur "true" pour réduire l'empreinte mémoire des opérations d'enregistrement de documents volumineux
// au prix d'une augmentation de la durée de l'opération.
// Définissez la propriété "MemoryOptimization" sur "false" pour enregistrer normalement le document au format PDF.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Voir également

* class [SaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../saveoptions/)
* Assemblée [Aspose.Words](../../../)


