---
title: "Aspose::Words::LowCode::Splitter classe"
linktitle: "Splitter"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LowCode::Splitter classe. Fournit des méthodes destinées à diviser les documents en parties en utilisant différents critères en C++."
type: docs
weight: 1500
url: /fr/cpp/aspose.words.lowcode/splitter/
---
## Splitter class


Fournit des méthodes destinées à diviser les documents en parties en utilisant différents critères.

```cpp
class Splitter : public Aspose::Words::LowCode::Processor
```

## Méthodes

| Méthode | Description |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::SplitterContext\>\&) | Crée une nouvelle instance du processeur de division. |
| [Execute](../processor/execute/)() | Exécutez l'action du processeur. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Exécutez l'action du processeur permettant d'annuler la tâche de traitement de document à l'aide du jeton d'annulation spécifié. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, int32_t, int32_t) | Extrait une plage spécifiée de pages d'un fichier de document et enregistre les pages extraites dans un nouveau fichier. Le format du fichier de sortie est déterminé par l'extension du nom du fichier de sortie. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Extrait une plage spécifiée de pages d'un fichier de document et enregistre les pages extraites dans un nouveau fichier en utilisant le format d'enregistrement spécifié. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Extrait une plage spécifiée de pages d'un fichier de document et enregistre les pages extraites dans un nouveau fichier en utilisant le format d'enregistrement spécifié. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Extrait une plage spécifiée de pages d'un flux de document et enregistre les pages extraites dans un flux de sortie en utilisant le format d'enregistrement spécifié. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Extrait une plage spécifiée de pages d'un flux de document et enregistre les pages extraites dans un flux de sortie en utilisant le format d'enregistrement spécifié. |
| [From](../processor/from/)(const System::String\&) | Spécifie le document d'entrée pour le traitement. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Spécifie le document d'entrée pour le traitement. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Spécifie le document d'entrée pour le traitement. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Spécifie le document d'entrée pour le traitement. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&) | Supprime les pages vides du document et enregistre la sortie. Retourne une liste des numéros de pages qui ont été supprimés. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Supprime les pages vides du document et enregistre la sortie dans le format spécifié. Retourne une liste des numéros de pages qui ont été supprimés. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Supprime les pages vides du document et enregistre la sortie dans le format spécifié. Retourne une liste des numéros de pages qui ont été supprimés. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Supprime les pages blanches d'un document fourni dans un flux d'entrée et enregistre le document mis à jour dans un flux de sortie au format d'enregistrement spécifié. Retourne une liste des numéros de pages qui ont été supprimés. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Supprime les pages blanches d'un document fourni dans un flux d'entrée et enregistre le document mis à jour dans un flux de sortie au format d'enregistrement spécifié. Retourne une liste des numéros de pages qui ont été supprimés. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Divise un document en plusieurs parties en fonction des options de division spécifiées et enregistre les parties résultantes dans des fichiers. Le format du fichier de sortie est déterminé par l'extension du nom du fichier de sortie. |
| static [Split](./split/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Divise un document en plusieurs parties en fonction des options de division spécifiées et enregistre les parties résultantes dans des fichiers au format d'enregistrement spécifié. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Divise un document en plusieurs parties en fonction des options de division spécifiées et enregistre les parties résultantes dans des fichiers au format d'enregistrement spécifié. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Divise un document provenant d'un flux d'entrée en plusieurs parties en fonction des options de division spécifiées et renvoie les parties résultantes sous forme d'un tableau de flux au format d'enregistrement spécifié. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Divise un document provenant d'un flux d'entrée en plusieurs parties en fonction des options de division spécifiées et renvoie les parties résultantes sous forme d'un tableau de flux au format d'enregistrement spécifié. |
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
