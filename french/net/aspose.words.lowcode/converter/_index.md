---
title: Converter Class
linktitle: Converter
articleTitle: Converter
second_title: Aspose.Words pour .NET
description: Convertissez facilement différents types de documents avec Aspose.Words.LowCode.Converter. Simplifiez votre flux de travail avec une seule ligne de code pour une intégration fluide.
type: docs
weight: 4230
url: /fr/net/aspose.words.lowcode/converter/
---
## Converter class

Représente un groupe de méthodes destinées à convertir une variété de types de documents différents à l'aide d'une seule ligne de code.

```csharp
public class Converter : Processor
```

## Méthodes

| Nom | La description |
| --- | --- |
| static [Create](../../aspose.words.lowcode/converter/create/#create)() | Crée une nouvelle instance du processeur de conversion. |
| static [Create](../../aspose.words.lowcode/converter/create/#create_1)(*[ConverterContext](../convertercontext/)*) | Crée une nouvelle instance du processeur de conversion. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Exécutez l'action du processeur. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Spécifie le document d'entrée pour le traitement. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Spécifie le document d'entrée pour le traitement. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Spécifie la liste des flux de documents de sortie. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spécifie la liste des flux de documents de sortie. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Spécifie le flux de sortie pour le processeur. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spécifie le flux de sortie pour le processeur. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Spécifie le fichier de sortie pour le processeur. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Spécifie le fichier de sortie pour le processeur. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_4)(*string, string*) | Convertit le document d'entrée donné en document de sortie en utilisant les noms de fichiers d'entrée-sortie spécifiés et leurs extensions. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Convertit le document d'entrée donné en un seul document de sortie à l'aide des flux d'entrée et de sortie spécifiés. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Convertit le document d'entrée donné en un seul document de sortie à l'aide des flux d'entrée et de sortie spécifiés. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Convertit le document d'entrée donné en document de sortie en utilisant les noms de fichiers d'entrée-sortie spécifiés et le format du document final. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Convertit le document d'entrée donné en document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés et les options d'enregistrement. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Convertit le document d'entrée donné en un seul document de sortie à l'aide des flux d'entrée et de sortie spécifiés. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Convertit le document d'entrée donné en document de sortie en utilisant les noms de fichiers d'entrée/sortie spécifiés et ses options de chargement/enregistrement. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_1)(*[Document](../../aspose.words/document/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Convertit les pages du document spécifié en images à l'aide des options d'enregistrement spécifiées et renvoie un tableau de flux contenant les images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages)(*[Document](../../aspose.words/document/), [SaveFormat](../../aspose.words/saveformat/)*) | Convertit les pages du document spécifié en images au format spécifié et renvoie un tableau de flux contenant les images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_4)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Convertit les pages du flux d'entrée spécifié en images à l'aide des options d'enregistrement spécifiées et renvoie un tableau de flux contenant les images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_3)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Convertit les pages du flux d'entrée spécifié en images au format spécifié et renvoie un tableau de flux contenant les images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_6)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Convertit les pages du fichier d'entrée spécifié en images à l'aide des options d'enregistrement spécifiées et renvoie un tableau de flux contenant les images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_5)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Convertit les pages du fichier d'entrée spécifié en images au format spécifié et renvoie un tableau de flux contenant les images. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Convertit les pages du flux d'entrée spécifié en images à l'aide des options de chargement et d'enregistrement fournies et renvoie un tableau de flux contenant les images. |

## Remarques

Les fichiers ou flux d'entrée et de sortie spécifiés, ainsi que le format d'enregistrement souhaité, sont utilisés pour convertir le document d'entrée donné d'un format en document de sortie de l'autre format spécifié.

La fonctionnalité de conversion prend en charge plus de 35 formats de fichiers différents.

Le[`ConvertToImages`](./converttoimages/)Un groupe de méthodes est conçu pour transformer des documents en images, chaque page étant convertie en un fichier image distinct. Ces méthodes convertissent également les documents PDF directement au format de page fixe, sans les charger dans le modèle de document, ce qui améliore les performances et la précision.

Avec[`PageSet`](../../aspose.words.saving/imagesaveoptions/pageset/), vous pouvez spécifier un ensemble particulier de pages à convertir en images.

### Voir également

* class [Processor](../processor/)
* espace de noms [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../)
