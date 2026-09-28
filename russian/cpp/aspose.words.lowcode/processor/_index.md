---
title: "Aspose::Words::LowCode::Processor class"
linktitle: "Processor"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::Processor класс. Класс процессора для выполнения различных действий по обработке документов на C++."
type: docs
weight: 1126
url: /ru/cpp/aspose.words.lowcode/processor/
---
## Processor class


[Processor](./) class for performing different document processing actions.

```cpp
class Processor : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Execute](./execute/)() | Выполнить действие процессора. |
| [Execute](./execute/)(System::Threading::CancellationToken) | Выполнить действие процессора, позволяя отменить задачу обработки документа с использованием указанного токена отмены. |
| [From](./from/)(const System::String\&) | Указывает входной документ для обработки. |
| [From](./from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Указывает входной документ для обработки. |
| [From](./from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Указывает входной документ для обработки. |
| [From](./from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Указывает входной документ для обработки. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [To](./to/)(const System::String\&) | Указывает выходной файл для процессора. |
| [To](./to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Указывает выходной файл для процессора. |
| [To](./to/)(const System::String\&, Aspose::Words::SaveFormat) | Указывает выходной файл для процессора. |
| [To](./to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Указывает выходной поток для процессора. |
| [To](./to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Указывает выходной поток для процессора. |
| [To](./to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](./to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
