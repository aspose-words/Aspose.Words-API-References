---
title: "Aspose::Words::LowCode::ComparerContext класс"
linktitle: "ComparerContext"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::ComparerContext класс. Контекст сравнения документов в C++."
type: docs
weight: 550
url: /ru/cpp/aspose.words.lowcode/comparercontext/
---
## ComparerContext class


[Document](../../aspose.words/document/) comparer context.

```cpp
class ComparerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Методы

| Метод | Описание |
| --- | --- |
| [ComparerContext](./comparercontext/)() |  |
| [get_AcceptRevisions](./get_acceptrevisions/)() const | Указывает, следует ли принимать исправления в документах перед их сравнением. Если сравниваемые документы содержат исправления и этот флаг установлен в false, процессор отклонит исправления. По умолчанию **true**. |
| [get_Author](./get_author/)() const | Автор, который будет назначен для исправлений, созданных во время сравнения документов. |
| [get_CompareOptions](./get_compareoptions/)() const | Параметры, используемые при сравнении документов. |
| [get_DateTime](./get_datetime/)() const | Дата и время, назначенные для исправлений, созданных во время сравнения документов. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Настройки [Font](../../aspose.words/font/) используемые процессором. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Параметры макета [Document](../../aspose.words/document/) используемые процессором. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Обратный вызов предупреждения, используемый процессором. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_AcceptRevisions](./set_acceptrevisions/)(bool) | Указывает, следует ли принимать исправления в документах перед их сравнением. Если сравниваемые документы содержат исправления и этот флаг установлен в false, процессор отклонит исправления. По умолчанию **true**. |
| [set_Author](./set_author/)(const System::String\&) | Автор, который будет назначен для исправлений, созданных во время сравнения документов. |
| [set_DateTime](./set_datetime/)(System::DateTime) | Дата и время, назначенные для исправлений, созданных во время сравнения документов. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Настройки [Font](../../aspose.words/font/) используемые процессором. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Обратный вызов предупреждения, используемый процессором. |
| static [Type](./type/)() |  |
## См. также

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
