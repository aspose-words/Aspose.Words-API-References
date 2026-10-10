---
title: "Aspose::Words::LowCode::Comparer classe"
linktitle: "Comparer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LowCode::Comparer classe. Fournit des méthodes destinées à comparer des documents en C++."
type: docs
weight: 500
url: /fr/cpp/aspose.words.lowcode/comparer/
---
## Comparer class


Fournit des méthodes destinées à comparer des documents.

```cpp
class Comparer : public Aspose::Words::LowCode::Processor
```

## Méthodes

| Méthode | Description |
| --- | --- |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) | Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié, produisant des modifications sous forme d'un nombre de révisions d'édition et de format. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié, produisant des modifications sous forme d'un nombre de révisions d'édition et de format. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié au format d'enregistrement fourni, produisant des modifications sous forme d'un nombre de révisions d'édition et de format. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié au format d'enregistrement fourni, produisant des modifications sous forme d'un nombre de révisions d'édition et de format. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié au format d'enregistrement fourni, produisant des modifications sous forme d'un nombre de révisions d'édition et de format. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié au format d'enregistrement fourni, produisant des modifications sous forme d'un nombre de révisions d'édition et de format. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | Compare deux documents chargés à partir de flux avec des options supplémentaires et enregistre les différences dans le flux de sortie fourni au format d'enregistrement spécifié, produisant des modifications sous forme d'un nombre de révisions d'édition et de format. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compare deux documents chargés à partir de flux avec des options supplémentaires et enregistre les différences dans le flux de sortie fourni au format d'enregistrement spécifié, produisant des modifications sous forme d'un nombre de révisions d'édition et de format. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | Compare deux documents chargés à partir de flux avec des options supplémentaires et enregistre les différences dans le flux de sortie fourni au format d'enregistrement spécifié, produisant des modifications sous forme d'un nombre de révisions d'édition et de format. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compare deux documents chargés à partir de flux avec des options supplémentaires et enregistre les différences dans le flux de sortie fourni au format d'enregistrement spécifié, produisant des modifications sous forme d'un nombre de révisions d'édition et de format. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau retourné représente une page unique de la sortie rendue sous forme d'image. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau retourné représente une page unique de la sortie rendue sous forme d'image. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau retourné représente une page unique de la sortie rendue sous forme d'image. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compare deux documents et enregistre les différences sous forme d'images. Chaque élément du tableau retourné représente une page unique de la sortie rendue sous forme d'image. |
| static [Create](./create/)() | Crée une nouvelle instance du processeur de conversion. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ComparerContext\>\&) | Crée une nouvelle instance du processeur de comparaison. |
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
## Voir aussi

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
