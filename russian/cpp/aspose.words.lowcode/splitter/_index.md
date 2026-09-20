---
title: "Aspose::Words::LowCode::Splitter класс"
linktitle: "Splitter"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::Splitter класс. Предоставляет методы, предназначенные для разделения документов на части с использованием различных критериев в C++."
type: docs
weight: 1500
url: /ru/cpp/aspose.words.lowcode/splitter/
---
## Splitter class


Предоставляет методы, предназначенные для разбивки документов на части с использованием различных критериев.

```cpp
class Splitter : public Aspose::Words::LowCode::Processor
```

## Методы

| Метод | Описание |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::SplitterContext\>\&) | Создаёт новый экземпляр процессора‑разделителя. |
| [Execute](../processor/execute/)() | Выполнить действие процессора. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Выполнить действие процессора, позволяя отменить задачу обработки документа с использованием указанного токена отмены. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, int32_t, int32_t) | Извлекает указанный диапазон страниц из файла документа и сохраняет извлечённые страницы в новый файл. Формат выходного файла определяется расширением имени выходного файла. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Извлекает указанный диапазон страниц из файла документа и сохраняет извлечённые страницы в новый файл, используя указанный формат сохранения. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Извлекает указанный диапазон страниц из файла документа и сохраняет извлечённые страницы в новый файл, используя указанный формат сохранения. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Извлекает указанный диапазон страниц из потока документа и сохраняет извлечённые страницы в выходной поток, используя указанный формат сохранения. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Извлекает указанный диапазон страниц из потока документа и сохраняет извлечённые страницы в выходной поток, используя указанный формат сохранения. |
| [From](../processor/from/)(const System::String\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Указывает входной документ для обработки. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&) | Удаляет пустые страницы из документа и сохраняет результат. Возвращает список номеров удалённых страниц. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Удаляет пустые страницы из документа и сохраняет результат в указанном формате. Возвращает список номеров удалённых страниц. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Удаляет пустые страницы из документа и сохраняет результат в указанном формате. Возвращает список номеров удалённых страниц. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Удаляет пустые страницы из документа, предоставленного во входном потоке, и сохраняет обновлённый документ в выходной поток в указанном формате сохранения. Возвращает список номеров удалённых страниц. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Удаляет пустые страницы из документа, предоставленного во входном потоке, и сохраняет обновлённый документ в выходной поток в указанном формате сохранения. Возвращает список номеров удалённых страниц. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Разделяет документ на несколько частей на основе указанных параметров разделения и сохраняет полученные части в файлы. Формат выходного файла определяется расширением имени выходного файла. |
| static [Split](./split/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Разделяет документ на несколько частей на основе указанных параметров разделения и сохраняет полученные части в файлы в указанном формате сохранения. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Разделяет документ на несколько частей на основе указанных параметров разделения и сохраняет полученные части в файлы в указанном формате сохранения. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Разделяет документ из входного потока на несколько частей на основе указанных параметров разделения и возвращает полученные части в виде массива потоков в указанном формате сохранения. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Разделяет документ из входного потока на несколько частей на основе указанных параметров разделения и возвращает полученные части в виде массива потоков в указанном формате сохранения. |
| [To](../processor/to/)(const System::String\&) | Указывает выходной файл для процессора. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Указывает выходной файл для процессора. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Указывает выходной файл для процессора. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Указывает выходной поток для процессора. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Указывает выходной поток для процессора. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## См. также

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
