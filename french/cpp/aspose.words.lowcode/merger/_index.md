---
title: "Classe Aspose::Words::LowCode::Merger"
linktitle: "Merger"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::LowCode::Merger. Représente un groupe de méthodes destinées à fusionner une variété de différents types de documents en un seul document de sortie en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.lowcode/merger/
---
## Merger class


Représente un groupe de méthodes destinées à fusionner une variété de différents types de documents en un seul document de sortie.

```cpp
class Merger : public Aspose::Words::LowCode::Processor
```

## Méthodes

| Méthode | Description |
| --- | --- |
| static [Create](./create/)() | Crée une nouvelle instance du processeur de fusion de courrier. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::MergerContext\>\&) | Crée une nouvelle instance du processeur de fusion de courrier. |
| [Execute](../processor/execute/)() | Exécutez l'action du processeur. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Exécutez l'action du processeur permettant d'annuler la tâche de traitement de document à l'aide du jeton d'annulation spécifié. |
| [From](../processor/from/)(const System::String\&) | Spécifie le document d'entrée pour le traitement. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Spécifie le document d'entrée pour le traitement. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Spécifie le document d'entrée pour le traitement. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Spécifie le document d'entrée pour le traitement. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Fusionne les documents d'entrée fournis en un seul document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés avec [KeepSourceFormatting](../mergeformatmode/). |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, Aspose::Words::SaveFormat, Aspose::Words::LowCode::MergeFormatMode) | Fusionne les documents d'entrée fournis en un seul document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés ainsi que le format final du document. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusionne les documents d'entrée fournis en un seul document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés et les options d'enregistrement. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusionne les documents d'entrée fournis en un seul document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés et les options d'enregistrement. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusionne les documents d'entrée fournis en un seul document et renvoie une instance de [Document](../../aspose.words/document/) du document final. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusionne les documents d'entrée fournis en un seul document et renvoie une instance de [Document](../../aspose.words/document/) du document final. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusionne les documents d'entrée fournis en un seul document et renvoie une instance de [Document](../../aspose.words/document/) du document final. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::SaveFormat) | Fusionne les documents d'entrée fournis en un seul document de sortie en utilisant les flux d'entrée et de sortie spécifiés ainsi que le format final du document. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusionne les documents d'entrée fournis en un seul document de sortie en utilisant les flux d'entrée et de sortie spécifiés et les options d'enregistrement. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusionne les documents d'entrée fournis en un seul document de sortie en utilisant les flux d'entrée et de sortie spécifiés et les options d'enregistrement. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusionne les documents d'entrée fournis en un seul document et renvoie une instance de [Document](../../aspose.words/document/) du document final. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusionne les documents d'entrée fournis en un seul document et renvoie une instance de [Document](../../aspose.words/document/) du document final. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusionne les documents d'entrée fournis en un seul document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés et les options d'enregistrement. Rend la sortie sous forme d'images. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusionne les flux de documents d'entrée fournis en un seul document de sortie en utilisant les options d'enregistrement d'image spécifiées. Rend la sortie sous forme d'images. |
| [To](../processor/to/)(const System::String\&) | Spécifie le fichier de sortie pour le processeur. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Spécifie le fichier de sortie pour le processeur. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Spécifie le fichier de sortie pour le processeur. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Spécifie le flux de sortie pour le processeur. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Spécifie le flux de sortie pour le processeur. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Remarques


Les fichiers ou flux d'entrée et de sortie spécifiés, ainsi que les options de fusion et d'enregistrement souhaitées, sont utilisés pour fusionner les documents d'entrée fournis en un seul document de sortie.

La fonctionnalité de fusion prend en charge plus de 35 formats de fichiers différents.
## Voir aussi

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
