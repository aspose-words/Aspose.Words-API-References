---
title: RtfSaveOptions.ExportCompactSize
linktitle: ExportCompactSize
articleTitle: ExportCompactSize
second_title: Aspose.Words pour .NET
description: Optimisez la taille des documents RTF grâce à la propriété ExportCompactSize. Assurez un stockage efficace tout en préservant l'intégrité du texte, même avec du contenu RTL.
type: docs
weight: 20
url: /fr/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

Permet de réduire la taille des documents RTF de sortie, mais s'ils contiennent du texte RTL (de droite à gauche), il ne s'affichera pas correctement. La valeur par défaut est`FAUX` .

```csharp
public bool ExportCompactSize { get; set; }
```

## Remarques

Si le document que vous souhaitez convertir en RTF à l'aide d'Aspose.Words ne contient pas de texte de droite à gauche dans des langues comme l'arabe, vous pouvez définir cette option sur`vrai` pour réduire la taille du RTF résultant.

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
