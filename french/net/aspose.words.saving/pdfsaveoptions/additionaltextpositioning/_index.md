---
title: PdfSaveOptions.AdditionalTextPositioning
linktitle: AdditionalTextPositioning
articleTitle: AdditionalTextPositioning
second_title: Aspose.Words pour .NET
description: Découvrez la propriété PdfSaveOptions AdditionalTextPositioning pour contrôler le positionnement du texte dans les PDF. Améliorez la mise en page de votre document sans effort !
type: docs
weight: 20
url: /fr/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

Un indicateur spécifiant s'il faut écrire ou non des opérateurs de positionnement de texte supplémentaires.

```csharp
public bool AdditionalTextPositioning { get; set; }
```

## Remarques

Si`vrai` Des opérateurs de positionnement de texte supplémentaires sont ajoutés au PDF de sortie. Cela peut permettre de résoudre les problèmes de positionnement de texte inexact sur certaines imprimantes. L'inconvénient est l'augmentation de la taille du document PDF.

La valeur par défaut est`FAUX`.

## Exemples

Montrez comment écrire des opérateurs de positionnement de texte supplémentaires.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// Créez un objet « PdfSaveOptions » que nous pouvons transmettre à la méthode « Save » du document
// pour modifier la manière dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // Définissez la propriété « AdditionalTextPositioning » sur « true » pour tenter de corriger une erreur
    // positionnement des éléments dans le PDF de sortie, s'il y en a, au prix d'une augmentation de la taille du fichier.
    // Définissez la propriété « AdditionalTextPositioning » sur « false » pour restituer le document comme d'habitude.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
