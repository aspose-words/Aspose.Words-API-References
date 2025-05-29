---
title: ReportBuilder Class
linktitle: ReportBuilder
articleTitle: ReportBuilder
second_title: Aspose.Words pour .NET
description: Créez facilement des rapports dynamiques avec Aspose.Words LowCode ReportBuilder. Utilisez le moteur de création de rapports LINQ pour remplir vos modèles avec des données en toute fluidité.
type: docs
weight: 4360
url: /fr/net/aspose.words.lowcode/reportbuilder/
---
## ReportBuilder class

Fournit des méthodes destinées à remplir le modèle avec des données à l'aide de LINQ Reporting Engine.

```csharp
public class ReportBuilder : Processor
```

## Méthodes

| Nom | La description |
| --- | --- |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create)() | Crée une nouvelle instance du processeur de création de rapports. |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create_1)(*[ReportBuilderContext](../reportbuildercontext/)*) | Crée une nouvelle instance du processeur de création de rapports. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Exécutez l'action du processeur. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Spécifie le document d'entrée pour le traitement. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Spécifie le document d'entrée pour le traitement. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Spécifie la liste des flux de documents de sortie. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spécifie la liste des flux de documents de sortie. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Spécifie le flux de sortie pour le processeur. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spécifie le flux de sortie pour le processeur. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Spécifie le fichier de sortie pour le processeur. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spécifie le fichier de sortie pour le processeur. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_12)(*string, string, object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec des options supplémentaires. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec le format de sortie spécifié et des options supplémentaires, à partir des flux d'entrée et de sortie. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec le format de sortie spécifié et des options supplémentaires, à partir des flux d'entrée et de sortie. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_13)(*string, string, object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec une référence de source de données nommée et des options supplémentaires. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_14)(*string, string, object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec des données provenant de plusieurs sources, générant un rapport complet avec des options supplémentaires. Cette surcharge détermine automatiquement le format d'enregistrement en fonction de l'extension du fichier de sortie. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_6)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec le format de sortie spécifié et des options supplémentaires. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_9)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec le format de sortie spécifié et des options supplémentaires. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec une référence de source de données nommée et des options supplémentaires. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_2)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec des données provenant de plusieurs sources, générant un rapport terminé avec le format de sortie spécifié et des options supplémentaires à partir des flux de fichiers d'entrée et de sortie spécifiés. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_4)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec une référence de source de données nommée et des options supplémentaires. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_5)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec des données provenant de plusieurs sources, générant un rapport terminé avec le format de sortie spécifié et des options supplémentaires à partir des flux de fichiers d'entrée et de sortie spécifiés. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_7)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec le format de sortie spécifié, une référence de source de données nommée et des options supplémentaires. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_8)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec des données provenant de plusieurs sources, générant un rapport terminé avec un format de sortie spécifié et des options supplémentaires. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_10)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec les données de la source spécifiée, générant un rapport terminé avec le format de sortie spécifié, une référence de source de données nommée et des options supplémentaires. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_11)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec des données provenant de plusieurs sources, générant un rapport terminé avec un format de sortie spécifié et des options supplémentaires. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec des données provenant de plusieurs sources. Restitue la sortie sous forme d'images. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages_1)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Remplit le document modèle avec des données provenant de plusieurs sources. Restitue la sortie sous forme d'images. |

### Voir également

* class [Processor](../processor/)
* espace de noms [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../)
