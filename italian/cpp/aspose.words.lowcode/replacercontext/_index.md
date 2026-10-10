---
title: "classe Aspose::Words::LowCode::ReplacerContext"
linktitle: "ReplacerContext"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::LowCode::ReplacerContext. Contesto dell'operazione di ricerca/sostituzione in C++."
type: docs
weight: 1292
url: /it/cpp/aspose.words.lowcode/replacercontext/
---
## ReplacerContext class


Contesto dell'operazione Trova/Sostituisci.

```cpp
class ReplacerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_FindReplaceOptions](./get_findreplaceoptions/)() const | Opzioni di ricerca/sostituzione. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Impostazioni [Font](../../aspose.words/font/) utilizzate dal processore. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Opzioni di layout [Document](../../aspose.words/document/) utilizzate dal processore. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Callback di avviso utilizzato dal processore. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [ReplacerContext](./replacercontext/)() |  |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Impostazioni [Font](../../aspose.words/font/) utilizzate dal processore. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Callback di avviso utilizzato dal processore. |
| [SetReplacement](./setreplacement/)(const System::String\&, const System::String\&) | Imposta il modello e la sostituzione utilizzati dall'operazione di ricerca/sostituzione. |
| [SetReplacement](./setreplacement/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Imposta il modello e la sostituzione utilizzati dall'operazione di ricerca/sostituzione. |
| static [Type](./type/)() |  |
## Vedi anche

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
