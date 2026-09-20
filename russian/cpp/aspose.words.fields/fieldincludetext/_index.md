---
title: "Aspose::Words::Fields::FieldIncludeText класс"
linktitle: "FieldIncludeText"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldIncludeText класс. Реализует поле INCLUDETEXT. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 58000
url: /ru/cpp/aspose.words.fields/fieldincludetext/
---
## FieldIncludeText class


Реализует поле INCLUDETEXT. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldIncludeText : public Aspose::Words::Fields::Field,
                         public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                         public Aspose::Words::Fields::IFieldIncludeTextCode
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() override | Получает имя закладки в документе для включения. |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_Encoding](./get_encoding/)() | Получает кодировку, применяемую к данным в указанном файле. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_LockFields](./get_lockfields/)() override | Получает, следует ли предотвращать обновление полей во включённом документе. |
| [get_MimeType](./get_mimetype/)() | Получает MIME‑тип указанного файла. |
| [get_NamespaceMappings](./get_namespacemappings/)() override | Получает сопоставления пространств имён для запросов XPath. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_Separator](../field/get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_SourceFullName](./get_sourcefullname/)() override | Получает расположение документа с использованием IRI. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| [get_TextConverter](./get_textconverter/)() override | Получает имя текстового конвертера для формата включённого файла. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [get_XPath](./get_xpath/)() override | Получает XPath для нужной части XML‑файла. |
| [get_XslTransformation](./get_xsltransformation/)() override | Получает расположение XSL‑трансформации для форматирования XML‑данных. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Устанавливает имя закладки в документе для включения. |
| [set_Encoding](./set_encoding/)(const System::String\&) | Устанавливает кодировку, применяемую к данным в указанном файле. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_LockFields](./set_lockfields/)(bool) | Устанавливает, следует ли предотвращать обновление полей во включённом документе. |
| [set_MimeType](./set_mimetype/)(const System::String\&) | Устанавливает MIME‑тип указанного файла. |
| [set_NamespaceMappings](./set_namespacemappings/)(const System::String\&) | Устанавливает сопоставления пространств имён для запросов XPath. |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Устанавливает расположение документа с использованием IRI. |
| [set_TextConverter](./set_textconverter/)(const System::String\&) | Устанавливает имя текстового конвертера для формата включённого файла. |
| [set_XPath](./set_xpath/)(const System::String\&) | Устанавливает XPath для нужной части XML‑файла. |
| [set_XslTransformation](./set_xsltransformation/)(const System::String\&) | Устанавливает расположение XSL‑трансформации для форматирования XML‑данных. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |
## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
