---
title: "Aspose::Words::LowCode::ReplacerContext classe"
linktitle: "ReplacerContext"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LowCode::ReplacerContext classe. Contexte d'opération de recherche/remplacement en C++."
type: docs
weight: 1292
url: /fr/cpp/aspose.words.lowcode/replacercontext/
---
## ReplacerContext class


Contexte d'opération de recherche/remplacement.

```cpp
class ReplacerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_FindReplaceOptions](./get_findreplaceoptions/)() const | Options de recherche/remplacement. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Paramètres de [Police](../../aspose.words/font/) utilisés par le processeur. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Options de mise en page du [Document](../../aspose.words/document/) utilisées par le processeur. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Rappel d'avertissement utilisé par le processeur. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [ReplacerContext](./replacercontext/)() |  |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Paramètres de [Police](../../aspose.words/font/) utilisés par le processeur. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Rappel d'avertissement utilisé par le processeur. |
| [SetReplacement](./setreplacement/)(const System::String\&, const System::String\&) | Définit le modèle et le remplacement utilisés par l'opération de recherche/remplacement. |
| [SetReplacement](./setreplacement/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Définit le modèle et le remplacement utilisés par l'opération de recherche/remplacement. |
| static [Type](./type/)() |  |
## Voir aussi

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
