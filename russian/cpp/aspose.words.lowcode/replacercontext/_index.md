---
title: "Aspose::Words::LowCode::ReplacerContext class"
linktitle: "ReplacerContext"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::ReplacerContext class. Контекст операции поиска/замены в C++."
type: docs
weight: 1292
url: /ru/cpp/aspose.words.lowcode/replacercontext/
---
## ReplacerContext class


Контекст операции поиска/замены.

```cpp
class ReplacerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_FindReplaceOptions](./get_findreplaceoptions/)() const | Параметры поиска/замены. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Настройки [Font](../../aspose.words/font/) используемые процессором. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Параметры макета [Document](../../aspose.words/document/) используемые процессором. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Обратный вызов предупреждения, используемый процессором. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [ReplacerContext](./replacercontext/)() |  |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Настройки [Font](../../aspose.words/font/) используемые процессором. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Обратный вызов предупреждения, используемый процессором. |
| [SetReplacement](./setreplacement/)(const System::String\&, const System::String\&) | Устанавливает шаблон и замену, используемые в операции поиска/замены. |
| [SetReplacement](./setreplacement/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Устанавливает шаблон и замену, используемые в операции поиска/замены. |
| static [Type](./type/)() |  |
## См. также

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
