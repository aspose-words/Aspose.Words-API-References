---
title: RtfSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words pour .NET
description: Découvrez la propriété RtfSaveOptions SaveFormat pour enregistrer sans effort vos documents au format RTF, garantissant ainsi la compatibilité et un partage facile.
type: docs
weight: 40
url: /fr/net/aspose.words.saving/rtfsaveoptions/saveformat/
---
## RtfSaveOptions.SaveFormat property

Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut êtreRtf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [RtfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
