---
title: Comparer Class
linktitle: Comparer
articleTitle: Comparer
second_title: Aspose.Words pour .NET
description: Comparez facilement des documents avec la classe Comparer LowCode d'Aspose.Words. Bénéficiez de méthodes puissantes pour une analyse et une collaboration fluides.
type: docs
weight: 4210
url: /fr/net/aspose.words.lowcode/comparer/
---
## Comparer class

Fournit des méthodes destinées à comparer des documents.

```csharp
public class Comparer : Processor
```

## Méthodes

| Nom | La description |
| --- | --- |
| static [Create](../../aspose.words.lowcode/comparer/create/#create)() | Crée une nouvelle instance du processeur de conversion. |
| static [Create](../../aspose.words.lowcode/comparer/create/#create_1)(*[ComparerContext](../comparercontext/)*) | Crée une nouvelle instance du processeur comparateur. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Exécutez l'action du processeur. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Spécifie le document d'entrée pour le traitement. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Spécifie le document d'entrée pour le traitement. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Spécifie la liste des flux de documents de sortie. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spécifie la liste des flux de documents de sortie. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Spécifie le flux de sortie pour le processeur. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spécifie le flux de sortie pour le processeur. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Spécifie le fichier de sortie pour le processeur. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spécifie le fichier de sortie pour le processeur. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_4)(*string, string, string, string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié, produisant des modifications sous forme de plusieurs révisions d'édition et de format. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare)(*Stream, Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Compare deux documents chargés à partir de flux avec des options supplémentaires et enregistre les différences dans le flux de sortie fourni dans le format d'enregistrement spécifié, produisant des modifications sous forme de nombre de révisions d'édition et de format. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_1)(*Stream, Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Compare deux documents chargés à partir de flux avec des options supplémentaires et enregistre les différences dans le flux de sortie fourni dans le format d'enregistrement spécifié, produisant des modifications sous forme de nombre de révisions d'édition et de format. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_2)(*string, string, string, [SaveFormat](../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié dans le format d'enregistrement fourni, produisant des modifications sous forme de plusieurs révisions d'édition et de format. |
| static [Compare](../../aspose.words.lowcode/comparer/compare/#compare_3)(*string, string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié dans le format d'enregistrement fourni, produisant des modifications sous forme de plusieurs révisions d'édition et de format. |
| static [CompareToImages](../../aspose.words.lowcode/comparer/comparetoimages/#comparetoimages)(*Stream, Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau renvoyé représente une seule page de la sortie rendue sous forme d'image. |
| static [CompareToImages](../../aspose.words.lowcode/comparer/comparetoimages/#comparetoimages_1)(*string, string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../aspose.words.comparing/compareoptions/)*) | Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau renvoyé représente une seule page de la sortie rendue sous forme d'image. |

### Voir également

* class [Processor](../processor/)
* espace de noms [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../)
