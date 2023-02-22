---
title: RtfSaveOptions.SaveFormat
second_title: Référence de l'API Aspose.Words pour .NET
description: RtfSaveOptions propriété. Spécifie le format dans lequel le document sera enregistré si cet objet doptions denregistrement est utilisé. Ne peut êtreRtf .
type: docs
weight: 40
url: /fr/net/aspose.words.saving/rtfsaveoptions/saveformat/
---
## RtfSaveOptions.SaveFormat property

Spécifie le format dans lequel le document sera enregistré si cet objet d'options d'enregistrement est utilisé. Ne peut êtreRtf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Exemples

Montre comment enregistrer un document au format .rtf avec des options personnalisées.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Créez un objet "RtfSaveOptions" à transmettre à la méthode "Save" du document pour modifier la façon dont nous l'enregistrons au format RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Définissez la propriété "ExportCompactSize" sur "true" pour
// réduit la taille du document enregistré au détriment de la compatibilité du texte de droite à gauche.
options.ExportCompactSize = true;

// Définissez la propriété "ExportImagesFotOldReaders" sur "true" pour utiliser des mots-clés supplémentaires afin de garantir que notre document est
// compatible avec les lecteurs pré-Microsoft Word 97 et WordPad.
// Définissez la propriété "ExportImagesFotOldReaders" à "false" pour réduire la taille du document,
// mais empêche les anciens lecteurs de lire les images non métafichiers ou BMP que le document peut contenir.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Voir également

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [RtfSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../rtfsaveoptions/)
* Assemblée [Aspose.Words](../../../)


