---
title: "Aspose::Words::LowCode::Watermarker classe"
linktitle: "Watermarker"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LowCode::Watermarker class. Fournit des méthodes destinées à insérer des filigranes dans les documents en C++."
type: docs
weight: 1750
url: /fr/cpp/aspose.words.lowcode/watermarker/
---
## Watermarker class


Fournit des méthodes destinées à insérer des filigranes dans les documents.

```cpp
class Watermarker : public Aspose::Words::LowCode::Processor
```

## Méthodes

| Méthode | Description |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::WatermarkerContext\>\&) | Crée une nouvelle instance du processeur de filigrane. |
| [Execute](../processor/execute/)() | Exécutez l'action du processeur. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Exécutez l'action du processeur permettant d'annuler la tâche de traitement de document à l'aide du jeton d'annulation spécifié. |
| [From](../processor/from/)(const System::String\&) | Spécifie le document d'entrée pour le traitement. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Spécifie le document d'entrée pour le traitement. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Spécifie le document d'entrée pour le traitement. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Spécifie le document d'entrée pour le traitement. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::String\&) | Ajoute un filigrane d'image dans le document. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Ajoute un filigrane d'image dans le document avec des options. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) | Ajoute un filigrane d'image dans le document avec des options et le format d'enregistrement spécifié. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Ajoute un filigrane d'image dans le document avec des options et le format d'enregistrement spécifié. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | Ajoute un filigrane d'image dans le document avec des options et le format d'enregistrement spécifié. |
| static [SetImage](./setimage/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Ajoute un filigrane d'image dans le document avec des options et le format d'enregistrement spécifié. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&) | Ajoute un filigrane d'image dans le document à partir de flux avec des options. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Ajoute un filigrane d'image dans le document à partir de flux avec des options. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&) | Ajoute un filigrane d'image dans le document à partir de flux avec des options. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Ajoute un filigrane d'image dans le document à partir de flux avec des options. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&) | Ajoute un filigrane d'image dans le document à partir de flux avec des options. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Ajoute un filigrane d'image dans le document à partir de flux avec des options. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Ajoute un filigrane d'image dans le document à partir de flux avec des options. |
| static [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Ajoute un filigrane d'image dans le document à partir de flux avec des options. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::String\&) | Ajoute un filigrane de texte dans le document. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Ajoute un filigrane de texte dans le document avec des options. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) | Ajoute un filigrane de texte dans le document avec des options et le format d'enregistrement spécifié. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Ajoute un filigrane de texte dans le document avec des options et le format d'enregistrement spécifié. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | Ajoute un filigrane de texte dans le document avec des options et le format d'enregistrement spécifié. |
| static [SetText](./settext/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Ajoute un filigrane de texte dans le document avec des options et le format d'enregistrement spécifié. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&) | Ajoute un filigrane de texte dans le document à partir de flux avec des options. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Ajoute un filigrane de texte dans le document à partir de flux avec des options. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) | Ajoute un filigrane de texte dans le document à partir de flux avec des options. |
| static [SetText](./settext/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Ajoute un filigrane de texte dans le document à partir de flux avec des options. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) | Ajoute un filigrane de texte dans le document avec des options. Rend la sortie en images. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Ajoute un filigrane de texte dans le document avec des options. Rend la sortie en images. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&) | Ajoute un filigrane de texte dans le document avec des options. Rend la sortie en images. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Ajoute un filigrane de texte dans le document avec des options. Rend la sortie en images. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&) | Ajoute un filigrane d'image dans le document avec des options. Rend la sortie en images. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::ArrayPtr\<uint8_t\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Ajoute un filigrane d'image dans le document avec des options. Rend la sortie en images. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Ajoute un filigrane d'image dans le document avec des options. Rend la sortie en images. |
| static [SetWatermarkToImages](./setwatermarktoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Ajoute un filigrane d'image dans le document avec des options. Rend la sortie en images. |
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
