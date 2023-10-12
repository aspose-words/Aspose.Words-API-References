---
title: PdfSaveOptions.AdditionalTextPositioning
second_title: Référence de l'API Aspose.Words pour .NET
description: PdfSaveOptions propriété. Un indicateur spécifiant sil faut écrire ou non des opérateurs de positionnement de texte supplémentaires.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

Un indicateur spécifiant s'il faut écrire ou non des opérateurs de positionnement de texte supplémentaires.

```csharp
public bool AdditionalTextPositioning { get; set; }
```

### Remarques

Si`vrai` , des opérateurs de positionnement de texte supplémentaires sont écrits dans le PDF de sortie. Cela peut aider à surmonter les problèmes liés au positionnement inexact du texte avec certaines imprimantes. L'inconvénient est l'augmentation de la taille du document PDF.

La valeur par défaut est`FAUX`.

### Exemples

Montrez comment écrire des opérateurs de positionnement de texte supplémentaires.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// Crée un objet "PdfSaveOptions" que l'on peut passer à la méthode "Save" du document
// pour modifier la façon dont cette méthode convertit le document en .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // Définissez la propriété "AdditionalTextPositioning" sur "true" pour tenter de corriger les erreurs
    // positionnement des éléments dans le PDF de sortie, s'il y en a, au prix d'une augmentation de la taille du fichier.
    // Définissez la propriété "AdditionalTextPositioning" sur "false" pour afficher le document comme d'habitude.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### Voir également

* class [PdfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../pdfsaveoptions/)
* Assemblée [Aspose.Words](../../../)


