---
title: "Aspose::Words::Fields::FieldCitation class"
linktitle: "FieldCitation"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldCitation class. Реализует поле CITATION. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 22000
url: /ru/cpp/aspose.words.fields/fieldcitation/
---
## FieldCitation class


Реализует поле CITATION. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldCitation : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_AnotherSourceTag](./get_anothersourcetag/)() | Получает значение, которое соответствует значению элемента **Tag** другого источника, включаемого в цитату. |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_FormatLanguageId](./get_formatlanguageid/)() | Получает идентификатор языка, который используется вместе с указанным библиографическим стилем для форматирования цитаты в документе. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_PageNumber](./get_pagenumber/)() | Получает номер страницы, связанный с цитатой. |
| [get_Prefix](./get_prefix/)() | Получает префикс, который добавляется перед цитатой. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_Separator](../field/get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_SourceTag](./get_sourcetag/)() | Получает значение, которое соответствует значению элемента **Tag** источника для вставки. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| [get_Suffix](./get_suffix/)() | Получает суффикс, который добавляется к цитате. |
| [get_SuppressAuthor](./get_suppressauthor/)() | Получает, скрыта ли информация об авторе в цитате. |
| [get_SuppressTitle](./get_suppresstitle/)() | Получает, скрыта ли информация о заголовке в цитате. |
| [get_SuppressYear](./get_suppressyear/)() | Получает, скрыта ли информация о годе в цитате. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [get_VolumeNumber](./get_volumenumber/)() | Получает номер тома, связанный с цитатой. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_AnotherSourceTag](./set_anothersourcetag/)(const System::String\&) | Устанавливает значение, которое соответствует значению элемента **Tag** другого источника, включаемого в цитату. |
| [set_FormatLanguageId](./set_formatlanguageid/)(const System::String\&) | Устанавливает идентификатор языка, который используется вместе с указанным библиографическим стилем для форматирования цитаты в документе. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumber](./set_pagenumber/)(const System::String\&) | Устанавливает номер страницы, связанный с цитатой. |
| [set_Prefix](./set_prefix/)(const System::String\&) | Устанавливает префикс, который добавляется перед цитатой. |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceTag](./set_sourcetag/)(const System::String\&) | Устанавливает значение, которое соответствует значению элемента **Tag** источника для вставки. |
| [set_Suffix](./set_suffix/)(const System::String\&) | Устанавливает суффикс, который добавляется к цитате. |
| [set_SuppressAuthor](./set_suppressauthor/)(bool) | Устанавливает, скрывать ли информацию об авторе в цитате. |
| [set_SuppressTitle](./set_suppresstitle/)(bool) | Устанавливает, скрывать ли информацию о заголовке в цитате. |
| [set_SuppressYear](./set_suppressyear/)(bool) | Устанавливает, скрывать ли информацию о годе в цитате. |
| [set_VolumeNumber](./set_volumenumber/)(const System::String\&) | Устанавливает номер тома, связанный с цитатой. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |
## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
