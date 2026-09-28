---
title: "Aspose::Words::LowCode::Replacer class"
linktitle: "Replacer"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::Replacer class. Предоставляет методы, предназначенные для поиска и замены текста в документе в C++."
type: docs
weight: 1250
url: /ru/cpp/aspose.words.lowcode/replacer/
---
## Replacer class


Предоставляет методы, предназначенные для поиска и замены текста в документе.

```cpp
class Replacer : public Aspose::Words::LowCode::Processor
```

## Методы

| Метод | Описание |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ReplacerContext\>\&) | Создаёт новый экземпляр процессора замен. |
| [Execute](../processor/execute/)() | Выполнить действие процессора. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Выполнить действие процессора, позволяя отменить задачу обработки документа с использованием указанного токена отмены. |
| [From](../processor/from/)(const System::String\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Указывает входной документ для обработки. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Указывает входной документ для обработки. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&) | Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном файле. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) | Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном файле, используя указанный формат сохранения и дополнительные параметры. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном файле, используя указанный формат сохранения и дополнительные параметры. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) | Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном файле, используя указанный формат сохранения и дополнительные параметры. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном файле, используя указанный формат сохранения и дополнительные параметры. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) | Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном потоке, используя указанный формат сохранения и дополнительные параметры. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном потоке, используя указанный формат сохранения и дополнительные параметры. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) | Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном потоке, используя указанный формат сохранения и дополнительные параметры. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном потоке, используя указанный формат сохранения и дополнительные параметры. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Заменяет все вхождения указанного строкового шаблона на строку‑замену во входном файле с использованием регулярного выражения. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами. |
| static [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном потоке, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном потоке, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном потоке, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами. |
| static [Replace](./replace/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном потоке, используя регулярное выражение, с указанным форматом сохранения и дополнительными параметрами. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) | Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле. Выводит результат в виде изображений. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле. Выводит результат в виде изображений. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&) | Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле. Выводит результат в виде изображений. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель во входном файле. Выводит результат в виде изображений. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Заменяет все вхождения указанного шаблона регулярного выражения на строку‑заменитель во входном файле. Выводит результат в виде изображений. |
| static [ReplaceToImages](./replacetoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Заменяет все вхождения указанного шаблона регулярного выражения на строку‑заменитель во входном файле. Выводит результат в виде изображений. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Заменяет все вхождения указанного шаблона регулярного выражения на строку‑заменитель во входном файле. Выводит результат в виде изображений. |
| static [ReplaceToImages](./replacetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Заменяет все вхождения указанного шаблона регулярного выражения на строку‑заменитель во входном файле. Выводит результат в виде изображений. |
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
