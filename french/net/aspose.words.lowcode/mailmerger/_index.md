---
title: MailMerger Class
linktitle: MailMerger
articleTitle: MailMerger
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.LowCode.MailMerger. Remplissez facilement vos modèles avec des données grâce à des techniques de publipostage simples et avancées pour une automatisation transparente de vos documents.
type: docs
weight: 4270
url: /fr/net/aspose.words.lowcode/mailmerger/
---
## MailMerger class

Fournit des méthodes destinées à remplir le modèle avec des données à l'aide d'opérations simples de publipostage et de publipostage avec des régions.

```csharp
public class MailMerger : Processor
```

## Méthodes

| Nom | La description |
| --- | --- |
| static [Create](../../aspose.words.lowcode/mailmerger/create/)(*[MailMergerContext](../mailmergercontext/)*) | Crée une nouvelle instance du processeur de publipostage. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Exécutez l'action du processeur. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Spécifie le document d'entrée pour le traitement. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Spécifie le document d'entrée pour le traitement. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Spécifie la liste des flux de documents de sortie. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spécifie la liste des flux de documents de sortie. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Spécifie le flux de sortie pour le processeur. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spécifie le flux de sortie pour le processeur. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Spécifie le fichier de sortie pour le processeur. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spécifie le fichier de sortie pour le processeur. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_12)(*string, string, DataRow*) | Effectue un publipostage à partir d'un DataRow dans le document. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_13)(*string, string, DataTable*) | Effectue un publipostage à partir d'un DataTable vers le document. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_14)(*string, string, string[], object[]*) | Effectue une opération de publipostage pour un seul enregistrement. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Effectue une opération de publipostage pour un seul enregistrement. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Effectue une opération de publipostage pour un seul enregistrement. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Effectue une opération de publipostage pour un seul enregistrement. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_4)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Effectue une opération de publipostage pour un seul enregistrement. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_6)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataRow dans le document. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_7)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataRow dans le document. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_9)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataRow dans le document. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_10)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataRow dans le document. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_2)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Effectue une opération de publipostage pour un seul enregistrement. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_5)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Effectue une opération de publipostage pour un seul enregistrement. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_8)(*string, string, [SaveFormat](../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Effectue une opération de publipostage pour un seul enregistrement. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_11)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Effectue une opération de publipostage pour un seul enregistrement. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataRow dans le document et restitue le résultat sous forme d'images. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_1)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataRow dans le document et restitue le résultat sous forme d'images. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_3)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataRow dans le document et restitue le résultat sous forme d'images. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_4)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataRow dans le document et restitue le résultat sous forme d'images. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_2)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Effectue une opération de publipostage pour un seul enregistrement et restitue le résultat sous forme d'images. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_5)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Effectue une opération de publipostage pour un seul enregistrement et restitue le résultat sous forme d'images. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_8)(*string, string, DataSet*) | Effectue un publipostage à partir d'un DataSet vers un document avec des régions de publipostage. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_9)(*string, string, DataTable*) | Effectue un publipostage à partir d'un DataTable dans le document avec des régions de publipostage. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataSet dans le document avec des régions de publipostage. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Effectue une opération de publipostage pour un seul enregistrement. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataSet dans le document avec des régions de publipostage. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Effectue une opération de publipostage pour un seul enregistrement. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_4)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataSet dans le document avec des régions de publipostage. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataTable dans le document avec des régions de publipostage. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataSet dans le document avec des régions de publipostage. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_7)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataTable dans le document avec des régions de publipostage. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Effectue le publipostage à partir d'un DataSet dans le document avec des régions de publipostage et restitue le résultat sous forme d'images. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages_1)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataTable dans le document avec des régions de publipostage et restitue le résultat sous forme d'images. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages_2)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Effectue le publipostage à partir d'un DataSet dans le document avec des régions de publipostage et restitue le résultat sous forme d'images. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages_3)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Effectue un publipostage à partir d'un DataTable dans le document avec des régions de publipostage et restitue le résultat sous forme d'images. |

### Voir également

* class [Processor](../processor/)
* espace de noms [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../)
