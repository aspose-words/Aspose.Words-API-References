---
title: "Aspose::Words::LowCode::Processor classe"
linktitle: "Processor"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LowCode::Processor classe. Classe de processeur pour effectuer différentes actions de traitement de documents en C++."
type: docs
weight: 1126
url: /fr/cpp/aspose.words.lowcode/processor/
---
## Processor class


[Processor](./) class for performing different document processing actions.

```cpp
class Processor : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Execute](./execute/)() | Exécutez l'action du processeur. |
| [Execute](./execute/)(System::Threading::CancellationToken) | Exécutez l'action du processeur permettant d'annuler la tâche de traitement de document à l'aide du jeton d'annulation spécifié. |
| [From](./from/)(const System::String\&) | Spécifie le document d'entrée pour le traitement. |
| [From](./from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Spécifie le document d'entrée pour le traitement. |
| [From](./from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Spécifie le document d'entrée pour le traitement. |
| [From](./from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Spécifie le document d'entrée pour le traitement. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [To](./to/)(const System::String\&) | Spécifie le fichier de sortie pour le processeur. |
| [To](./to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Spécifie le fichier de sortie pour le processeur. |
| [To](./to/)(const System::String\&, Aspose::Words::SaveFormat) | Spécifie le fichier de sortie pour le processeur. |
| [To](./to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Spécifie le flux de sortie pour le processeur. |
| [To](./to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Spécifie le flux de sortie pour le processeur. |
| [To](./to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](./to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
