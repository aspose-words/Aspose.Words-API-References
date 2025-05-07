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
class ReplacerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Methods

| Method | Description |
| --- | --- |
| [get_FindReplaceOptions](./get_findreplaceoptions/)() const | Find/replace options. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | [Font](../../aspose.words/font/) settings used by the processor. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | [Document](../../aspose.words/document/) layout options used by the processor. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Warning callback used by the processor. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [ReplacerContext](./replacercontext/)() |  |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | [Font](../../aspose.words/font/) settings used by the processor. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Warning callback used by the processor. |
| [SetReplacement](./setreplacement/)(const System::String\&, const System::String\&) | Sets pattern and replacement used by find/replace operation. |
| [SetReplacement](./setreplacement/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Sets pattern and replacement used by find/replace operation. |
| static [Type](./type/)() |  |
## See Also

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
