---
title: Aspose::Words::LowCode::ReplacerContext class
linktitle: ReplacerContext
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::ReplacerContext class. Find/replace operation context in C++.'
type: docs
weight: 1292
url: /cpp/aspose.words.lowcode/replacercontext/
---
## ReplacerContext class


Find/replace operation context.

```cpp
class ReplacerContext : public ProcessorContext
```

## Methods

| Method | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo \&) const override |  |
| [ReplacerContext](./replacercontext/)() |  |
| [SetReplacement](./setreplacement/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\> \&, const System::String \&) | Sets pattern and replacement used by find/replace operation. |
| [SetReplacement](./setreplacement/)(const System::String \&, const System::String \&) | Sets pattern and replacement used by find/replace operation. |
| static [Type](./type/)() |  |
| [get_FindReplaceOptions](./get_findreplaceoptions/)() const | Find/replace options. |
| [GetType](../processorcontext/gettype/)() const override |  |
| [Is](../processorcontext/is/)(const System::TypeInfo \&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| static [Type](../processorcontext/type/)() |  |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Font settings used by the processor. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Document layout options used by the processor. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Warning callback used by the processor. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\> \&) | Font settings used by the processor. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\> \&) | Warning callback used by the processor. |
## See Also

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
