---
title: "Aspose::Words::LowCode::ReplacerContext Klasse"
linktitle: "ReplacerContext"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::ReplacerContext Klasse. Kontext für Find/Replace-Operationen in C++."
type: docs
weight: 1292
url: /de/cpp/aspose.words.lowcode/replacercontext/
---
## ReplacerContext class


Suchen/Ersetzen‑Vorgangskontext.

```cpp
class ReplacerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_FindReplaceOptions](./get_findreplaceoptions/)() const | Find/Replace-Optionen. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | [Font](../../aspose.words/font/) Einstellungen, die vom Prozessor verwendet werden. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | [Document](../../aspose.words/document/) Layout-Optionen, die vom Prozessor verwendet werden. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Warnungs-Callback, der vom Prozessor verwendet wird. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [ReplacerContext](./replacercontext/)() |  |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | [Font](../../aspose.words/font/) Einstellungen, die vom Prozessor verwendet werden. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Warnungs-Callback, der vom Prozessor verwendet wird. |
| [SetReplacement](./setreplacement/)(const System::String\&, const System::String\&) | Legt das Muster und den Ersatz fest, die von der Find/Replace-Operation verwendet werden. |
| [SetReplacement](./setreplacement/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Legt das Muster und den Ersatz fest, die von der Find/Replace-Operation verwendet werden. |
| static [Type](./type/)() |  |
## Siehe auch

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
