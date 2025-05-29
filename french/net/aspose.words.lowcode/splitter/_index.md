---
title: Splitter Class
linktitle: Splitter
articleTitle: Splitter
second_title: Aspose.Words pour .NET
description: Divisez facilement vos documents avec la classe Aspose.Words.LowCode.Splitter. Utilisez des méthodes polyvalentes pour une gestion précise des documents et une efficacité accrue du flux de travail.
type: docs
weight: 4420
url: /fr/net/aspose.words.lowcode/splitter/
---
## Splitter class

Fournit des méthodes destinées à diviser les documents en parties en utilisant différents critères.

```csharp
public class Splitter : Processor
```

## Méthodes

| Nom | La description |
| --- | --- |
| static [Create](../../aspose.words.lowcode/splitter/create/)(*[SplitterContext](../splittercontext/)*) | Crée une nouvelle instance du processeur séparateur. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Exécutez l'action du processeur. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Spécifie le document d'entrée pour le traitement. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Spécifie le document d'entrée pour le traitement. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Spécifie la liste des flux de documents de sortie. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spécifie la liste des flux de documents de sortie. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Spécifie le flux de sortie pour le processeur. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spécifie le flux de sortie pour le processeur. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Spécifie le fichier de sortie pour le processeur. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spécifie le fichier de sortie pour le processeur. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_4)(*string, string, int, int*) | Extrait une plage de pages spécifiée d'un fichier document et enregistre les pages extraites dans un nouveau fichier. Le format du fichier de sortie est déterminé par l'extension du nom du fichier de sortie. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Extrait une plage spécifiée de pages d'un flux de documents et enregistre les pages extraites dans un flux de sortie en utilisant le format d'enregistrement spécifié. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Extrait une plage spécifiée de pages d'un flux de documents et enregistre les pages extraites dans un flux de sortie en utilisant le format d'enregistrement spécifié. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_2)(*string, string, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Extrait une plage spécifiée de pages d'un fichier de document et enregistre les pages extraites dans un nouveau fichier en utilisant le format d'enregistrement spécifié. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_3)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Extrait une plage spécifiée de pages d'un fichier de document et enregistre les pages extraites dans un nouveau fichier en utilisant le format d'enregistrement spécifié. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_2)(*string, string*) | Supprime les pages vides du document et enregistre le résultat. Renvoie la liste des numéros de page supprimés. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Supprime les pages vierges d'un document fourni dans un flux d'entrée et enregistre le document mis à jour dans un flux de sortie au format spécifié. Renvoie la liste des numéros de page supprimés. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Supprime les pages vierges d'un document fourni dans un flux d'entrée et enregistre le document mis à jour dans un flux de sortie au format spécifié. Renvoie la liste des numéros de page supprimés. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Supprime les pages vides du document et enregistre le résultat au format spécifié. Renvoie la liste des numéros de page supprimés. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Supprime les pages vides du document et enregistre le résultat au format spécifié. Renvoie la liste des numéros de page supprimés. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split)(*Stream, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Divise un document d'un flux d'entrée en plusieurs parties en fonction des options de division spécifiées et renvoie les parties résultantes sous forme de tableau de flux dans le format d'enregistrement spécifié. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Divise un document d'un flux d'entrée en plusieurs parties en fonction des options de division spécifiées et renvoie les parties résultantes sous forme de tableau de flux dans le format d'enregistrement spécifié. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_2)(*string, string, [SplitOptions](../splitoptions/)*) | Divise un document en plusieurs parties selon les options de division spécifiées et enregistre les parties obtenues dans des fichiers. Le format du fichier de sortie est déterminé par l'extension du nom du fichier de sortie. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Divise un document en plusieurs parties en fonction des options de division spécifiées et enregistre les parties résultantes dans des fichiers au format d'enregistrement spécifié. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Divise un document en plusieurs parties en fonction des options de division spécifiées et enregistre les parties résultantes dans des fichiers au format d'enregistrement spécifié. |

### Voir également

* class [Processor](../processor/)
* espace de noms [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../)
