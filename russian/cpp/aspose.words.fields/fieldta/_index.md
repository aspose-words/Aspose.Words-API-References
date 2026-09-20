---
title: "Aspose::Words::Fields::FieldTA класс"
linktitle: "FieldTA"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldTA класс. Реализует поле TA. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 99000
url: /ru/cpp/aspose.words.fields/fieldta/
---
## FieldTA class


Реализует поле TA. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldTA : public Aspose::Words::Fields::Field,
                public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_EntryCategory](./get_entrycategory/)() | Получает целую категорию записи, которая является числом, соответствующим порядку категорий. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_IsBold](./get_isbold/)() | Получает, следует ли применять полужирное форматирование к номеру страницы для записи. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsItalic](./get_isitalic/)() | Получает, следует ли применять курсивное форматирование к номеру страницы для записи. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_LongCitation](./get_longcitation/)() | Получает полную цитату для записи. |
| [get_PageRangeBookmarkName](./get_pagerangebookmarkname/)() | Получает имя закладки, которая отмечает диапазон страниц, вставляемый как номер страницы записи. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_Separator](../field/get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_ShortCitation](./get_shortcitation/)() | Получает краткую цитату для записи. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_EntryCategory](./set_entrycategory/)(const System::String\&) | Устанавливает целую категорию записи, которая является числом, соответствующим порядку категорий. |
| [set_IsBold](./set_isbold/)(bool) | Устанавливает, применять ли полужирное форматирование к номеру страницы записи. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsItalic](./set_isitalic/)(bool) | Устанавливает, применять ли курсивное форматирование к номеру страницы записи. |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_LongCitation](./set_longcitation/)(const System::String\&) | Устанавливает полную цитату для записи. |
| [set_PageRangeBookmarkName](./set_pagerangebookmarkname/)(const System::String\&) | Устанавливает имя закладки, которая отмечает диапазон страниц, вставляемый как номер страницы записи. |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_ShortCitation](./set_shortcitation/)(const System::String\&) | Устанавливает краткую цитату для записи. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |
## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
