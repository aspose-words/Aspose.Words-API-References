---
title: Merger.MergeToImages
linktitle: MergeToImages
articleTitle: MergeToImages
second_title: Aspose.Words pour .NET
description: Fusionnez plusieurs documents sans effort avec la méthode MergeToImages, en créant une sortie d'image unique tout en personnalisant les noms de fichiers et les options d'enregistrement.
type: docs
weight: 30
url: /fr/net/aspose.words.lowcode/merger/mergetoimages/
---
## MergeToImages(*string[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages_1}

Fusionne les documents d'entrée donnés en un seul document de sortie en utilisant les noms de fichiers d'entrée-sortie spécifiés et les options d'enregistrement. Restitue la sortie en images.

```csharp
public static Stream[] MergeToImages(string[] inputFiles, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputFiles | String[] | Les noms des fichiers d'entrée. |
| saveOptions | ImageSaveOptions | Les options de sauvegarde. |
| mergeFormatMode | MergeFormatMode | Spécifie comment fusionner les formats qui entrent en conflit. |

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)

---

## MergeToImages(*Stream[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages}

Fusionne les flux de documents d'entrée donnés en un seul document de sortie à l'aide des options d'enregistrement d'image spécifiées. Restitue la sortie en images.

```csharp
public static Stream[] MergeToImages(Stream[] inputStreams, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| inputStreams | Stream[] | Les flux de fichiers d'entrée. |
| saveOptions | ImageSaveOptions | Les options de sauvegarde. |
| mergeFormatMode | MergeFormatMode | Spécifie comment fusionner les formats qui entrent en conflit. |

### Voir également

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
