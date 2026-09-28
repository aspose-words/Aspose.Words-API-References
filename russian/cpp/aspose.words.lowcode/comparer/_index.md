---
title: "Aspose::Words::LowCode::Comparer class"
linktitle: "Comparer"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::Comparer class. Предоставляет методы, предназначенные для сравнения документов на C++."
type: docs
weight: 500
url: /ru/cpp/aspose.words.lowcode/comparer/
---
## Comparer class


Предоставляет методы, предназначенные для сравнения документов.

```cpp
class Comparer : public Aspose::Words::LowCode::Processor
```

## Методы

| Метод | Описание |
| --- | --- |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) | Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанный выходной файл, создавая изменения в виде ряда правок и форматных ревизий. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанный выходной файл, создавая изменения в виде ряда правок и форматных ревизий. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанный выходной файл в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанный выходной файл в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанный выходной файл в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Сравнивает два документа с дополнительными параметрами и сохраняет различия в указанный выходной файл в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | Сравнивает два документа, загруженных из потоков, с дополнительными параметрами и сохраняет различия в предоставленный выходной поток в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Сравнивает два документа, загруженных из потоков, с дополнительными параметрами и сохраняет различия в предоставленный выходной поток в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | Сравнивает два документа, загруженных из потоков, с дополнительными параметрами и сохраняет различия в предоставленный выходной поток в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Сравнивает два документа, загруженных из потоков, с дополнительными параметрами и сохраняет различия в предоставленный выходной поток в указанном формате сохранения, создавая изменения в виде ряда правок и форматных ревизий. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | Сравнивает два документа и сохраняет различия в виде изображений. Каждый элемент возвращаемого массива представляет отдельную страницу вывода, отрисованную как изображение. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Сравнивает два документа и сохраняет различия в виде изображений. Каждый элемент возвращаемого массива представляет отдельную страницу вывода, отрисованную как изображение. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | Сравнивает два документа и сохраняет различия в виде изображений. Каждый элемент возвращаемого массива представляет отдельную страницу вывода, отрисованную как изображение. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Сравнивает два документа и сохраняет различия в виде изображений. Каждый элемент возвращаемого массива представляет отдельную страницу вывода, отрисованную как изображение. |
| static [Create](./create/)() | Создает новый экземпляр процессора конвертера. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ComparerContext\>\&) | Создает новый экземпляр процессора сравнения. |
| [Execute](../processor/execute/)() | Выполнить действие процессора. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Выполнить действие процессора, позволяя отменить задачу обработки документа с использованием указанного токена отмены. |
| [From](../processor/from/)(const System::String\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Указывает входной документ для обработки. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
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
