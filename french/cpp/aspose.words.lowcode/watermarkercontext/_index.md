---
title: "classe Aspose::Words::LowCode::WatermarkerContext"
linktitle: "WatermarkerContext"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "classe Aspose::Words::LowCode::WatermarkerContext. Contexte de filigrane de document en C++."
type: docs
weight: 1875
url: /fr/cpp/aspose.words.lowcode/watermarkercontext/
---
## WatermarkerContext class


[Document](../../aspose.words/document/) watermarker context.

```cpp
class WatermarkerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Paramètres de [Police](../../aspose.words/font/) utilisés par le processeur. |
| [get_ImageWatermark](./get_imagewatermark/)() const | Octets d'image à utiliser comme filigrane. |
| [get_ImageWatermarkOptions](./get_imagewatermarkoptions/)() const | Options pour le filigrane de texte. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Options de mise en page du [Document](../../aspose.words/document/) utilisées par le processeur. |
| [get_TextWatermark](./get_textwatermark/)() const | Texte à utiliser comme filigrane. |
| [get_TextWatermarkOptions](./get_textwatermarkoptions/)() const | Options pour le filigrane d'image. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Rappel d'avertissement utilisé par le processeur. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Paramètres de [Police](../../aspose.words/font/) utilisés par le processeur. |
| [set_ImageWatermark](./set_imagewatermark/)(const System::ArrayPtr\<uint8_t\>\&) | Octets d'image à utiliser comme filigrane. |
| [set_TextWatermark](./set_textwatermark/)(const System::String\&) | Texte à utiliser comme filigrane. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Rappel d'avertissement utilisé par le processeur. |
| static [Type](./type/)() |  |
| [WatermarkerContext](./watermarkercontext/)() |  |
## Voir aussi

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
