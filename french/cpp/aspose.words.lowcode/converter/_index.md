---
title: "Classe Aspose::Words::LowCode::Converter"
linktitle: "Converter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::LowCode::Converter. Représente un groupe de méthodes destinées à convertir une variété de types de documents différents en utilisant une seule ligne de code en C++."
type: docs
weight: 600
url: /fr/cpp/aspose.words.lowcode/converter/
---
## Converter class


Représente un groupe de méthodes destinées à convertir une variété de différents types de documents en une seule ligne de code.

```cpp
class Converter : public Aspose::Words::LowCode::Processor
```

## Méthodes

| Méthode | Description |
| --- | --- |
| static [Convert](./convert/)(const System::String\&, const System::String\&) | Convertit le document d’entrée fourni en document de sortie en utilisant les noms de fichiers d’entrée et de sortie spécifiés ainsi que leurs extensions. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Convertit le document d'entrée donné en document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés et le format final du document. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Convertit le document d'entrée donné en document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés et les options d'enregistrement. |
| static [Convert](./convert/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Convertit le document d'entrée donné en document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés ainsi que ses options de chargement/enregistrement. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Convertit le document d'entrée donné en un seul document de sortie en utilisant les flux d'entrée et de sortie spécifiés. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Convertit le document d'entrée donné en un seul document de sortie en utilisant les flux d'entrée et de sortie spécifiés. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Convertit le document d'entrée donné en un seul document de sortie en utilisant les flux d'entrée et de sortie spécifiés. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&) | Convertit les pages du fichier d'entrée spécifié en fichiers image. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Convertit les pages du fichier d'entrée spécifié en fichiers image dans le format spécifié. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Convertit les pages du fichier d'entrée spécifié en fichiers image en utilisant les options d'enregistrement spécifiées. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Convertit les pages du fichier d'entrée spécifié en fichiers image en utilisant les options de chargement et d'enregistrement fournies. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, Aspose::Words::SaveFormat) | Convertit les pages du fichier d'entrée spécifié en images dans le format spécifié et renvoie un tableau de flux contenant les images. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Convertit les pages du fichier d'entrée spécifié en images en utilisant les options d'enregistrement spécifiées et renvoie un tableau de flux contenant les images. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Convertit les pages du flux d'entrée spécifié en images dans le format spécifié et renvoie un tableau de flux contenant les images. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Convertit les pages du flux d'entrée spécifié en images en utilisant les options d'enregistrement spécifiées et renvoie un tableau de flux contenant les images. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Convertit les pages du flux d'entrée spécifié en images en utilisant les options de chargement et d'enregistrement fournies, et renvoie un tableau de flux contenant les images. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) | Convertit les pages du document spécifié en images dans le format spécifié et renvoie un tableau de flux contenant les images. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Convertit les pages du document spécifié en images en utilisant les options d'enregistrement spécifiées et renvoie un tableau de flux contenant les images. |
| static [Create](./create/)() | Crée une nouvelle instance du processeur de conversion. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ConverterContext\>\&) | Crée une nouvelle instance du processeur de conversion. |
| [Execute](../processor/execute/)() | Exécutez l'action du processeur. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Exécutez l'action du processeur permettant d'annuler la tâche de traitement de document à l'aide du jeton d'annulation spécifié. |
| [From](../processor/from/)(const System::String\&) | Spécifie le document d'entrée pour le traitement. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Spécifie le document d'entrée pour le traitement. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Spécifie le document d'entrée pour le traitement. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Spécifie le document d'entrée pour le traitement. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [To](../processor/to/)(const System::String\&) | Spécifie le fichier de sortie pour le processeur. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Spécifie le fichier de sortie pour le processeur. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Spécifie le fichier de sortie pour le processeur. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Spécifie le flux de sortie pour le processeur. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Spécifie le flux de sortie pour le processeur. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Remarques


Les fichiers ou flux d'entrée et de sortie spécifiés, ainsi que le format d'enregistrement souhaité, sont utilisés pour convertir le document d'entrée donné d'un format en le document de sortie de l'autre format spécifié.

La fonctionnalité de conversion prend en charge plus de 35 formats de fichiers différents.

Le groupe de méthodes [ConvertToImages()](../) est conçu pour transformer les documents en images, chaque page étant convertie en un fichier image séparé. Ces méthodes convertissent également les documents PDF directement en formats à pages fixes sans les charger dans le modèle de document, ce qui améliore à la fois les performances et la précision.

Avec [PageSet](../../aspose.words.saving/imagesaveoptions/get_pageset/), vous pouvez spécifier un ensemble particulier de pages à convertir en images.
## Voir aussi

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
