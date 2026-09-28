---
title: "Класс Aspose::Words::LowCode::Merger"
linktitle: "Merger"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::LowCode::Merger. Представляет группу методов, предназначенных для объединения различных типов документов в один итоговый документ в C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.lowcode/merger/
---
## Merger class


Представляет набор методов, предназначенных для объединения различных типов документов в один итоговый документ.

```cpp
class Merger : public Aspose::Words::LowCode::Processor
```

## Методы

| Метод | Описание |
| --- | --- |
| static [Create](./create/)() | Создаёт новый экземпляр процессора слияния почты. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::MergerContext\>\&) | Создаёт новый экземпляр процессора слияния почты. |
| [Execute](../processor/execute/)() | Выполнить действие процессора. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Выполнить действие процессора, позволяя отменить задачу обработки документа с использованием указанного токена отмены. |
| [From](../processor/from/)(const System::String\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Указывает входной документ для обработки. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Объединяет указанные входные документы в один выходной документ, используя заданные имена входного и выходного файлов с помощью [KeepSourceFormatting](../mergeformatmode/). |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, Aspose::Words::SaveFormat, Aspose::Words::LowCode::MergeFormatMode) | Объединяет указанные входные документы в один выходной документ, используя заданные имена входного и выходного файлов и конечный формат документа. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Объединяет указанные входные документы в один выходной документ, используя заданные имена входного и выходного файлов и параметры сохранения. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Объединяет указанные входные документы в один выходной документ, используя заданные имена входного и выходного файлов и параметры сохранения. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, Aspose::Words::LowCode::MergeFormatMode) | Объединяет указанные входные документы в один документ и возвращает экземпляр [Document](../../aspose.words/document/) конечного документа. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Объединяет указанные входные документы в один документ и возвращает экземпляр [Document](../../aspose.words/document/) конечного документа. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Объединяет указанные входные документы в один документ и возвращает экземпляр [Document](../../aspose.words/document/) конечного документа. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::SaveFormat) | Объединяет указанные входные документы в один выходной документ, используя заданные входные и выходные потоки и конечный формат документа. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Объединяет указанные входные документы в один выходной документ, используя заданные входные и выходные потоки и параметры сохранения. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Объединяет указанные входные документы в один выходной документ, используя заданные входные и выходные потоки и параметры сохранения. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Объединяет указанные входные документы в один документ и возвращает экземпляр [Document](../../aspose.words/document/) конечного документа. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Объединяет указанные входные документы в один документ и возвращает экземпляр [Document](../../aspose.words/document/) конечного документа. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Объединяет указанные входные документы в один выходной документ, используя заданные имена входного и выходного файлов и параметры сохранения. Отображает вывод в виде изображений. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Объединяет указанные потоки входных документов в один выходной документ, используя заданные параметры сохранения изображений. Отображает вывод в виде изображений. |
| [To](../processor/to/)(const System::String\&) | Указывает выходной файл для процессора. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Указывает выходной файл для процессора. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Указывает выходной файл для процессора. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Указывает выходной поток для процессора. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Указывает выходной поток для процессора. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Примечания


Указанные входные и выходные файлы или потоки, вместе с желаемыми параметрами объединения и сохранения, используются для объединения указанных входных документов в один выходной документ.

Функция объединения поддерживает более 35 различных форматов файлов.
## См. также

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
