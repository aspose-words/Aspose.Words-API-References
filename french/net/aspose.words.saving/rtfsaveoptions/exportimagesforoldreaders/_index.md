---
title: RtfSaveOptions.ExportImagesForOldReaders
linktitle: ExportImagesForOldReaders
articleTitle: ExportImagesForOldReaders
second_title: Aspose.Words pour .NET
description: Optimisez vos documents RTF avec la propriété ExportImagesForOldReaders. Contrôlez l'inclusion de mots-clés pour les anciens lecteurs, ce qui impacte la taille du fichier et les performances.
type: docs
weight: 30
url: /fr/net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

Spécifie si les mots-clés pour les « anciens lecteurs » sont écrits au format RTF ou non. Cela peut affecter considérablement la taille du document RTF. La valeur par défaut est`vrai` .

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

## Remarques

Les « anciens lecteurs » sont des applications antérieures à Microsoft Word 97 et également WordPad. Lorsque cette option est`vrai` Aspose.Words écrit des mots-clés RTF supplémentaires. Ces mots-clés permettent au document de s'afficher correctement lorsqu'il est ouvert dans une application « ancien lecteur », mais peuvent augmenter considérablement la taille du document.

Si vous définissez cette option sur`FAUX`alors seules les images aux formats WMF, EMF et BMP seront affichées dans les "anciens lecteurs".

## Exemples

Montre comment enregistrer un document au format .rtf avec des options personnalisées.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Créez un objet « RtfSaveOptions » à transmettre à la méthode « Save » du document pour modifier la façon dont nous l'enregistrons dans un RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Définissez la propriété « ExportCompactSize » sur « true » pour
// réduire la taille du document enregistré au détriment de la compatibilité du texte de droite à gauche.
options.ExportCompactSize = true;

// Définissez la propriété « ExportImagesFotOldReaders » sur « true » pour utiliser des mots-clés supplémentaires afin de garantir que notre document est
// compatible avec les lecteurs pré-Microsoft Word 97 et WordPad.
// Définissez la propriété « ExportImagesFotOldReaders » sur « false » pour réduire la taille du document,
// mais empêche les anciens lecteurs de pouvoir lire les images non-métafichiers ou BMP que le document peut contenir.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Voir également

* class [RtfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
