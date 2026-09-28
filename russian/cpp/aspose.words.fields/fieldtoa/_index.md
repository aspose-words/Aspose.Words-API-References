---
title: "Aspose::Words::Fields::FieldToa класс"
linktitle: "FieldToa"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldToa класс. Реализует поле TOA. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 104000
url: /ru/cpp/aspose.words.fields/fieldtoa/
---
## FieldToa class


Реализует поле TOA. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldToa : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Получает имя закладки, которое отмечает часть документа, используемую для построения таблицы. |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_EntryCategory](./get_entrycategory/)() | Получает целую категорию для записей, включенных в таблицу. |
| [get_EntrySeparator](./get_entryseparator/)() | Получает последовательность символов, используемую для разделения записи таблицы указателей и её номера страницы. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_PageNumberListSeparator](./get_pagenumberlistseparator/)() | Получает последовательность символов, используемую для разделения двух номеров страниц в списке номеров страниц. |
| [get_PageRangeSeparator](./get_pagerangeseparator/)() | Получает последовательность символов, используемую для разделения начала и конца диапазона страниц. |
| [get_RemoveEntryFormatting](./get_removeentryformatting/)() | Получает, следует ли удалять форматирование текста записи в документе из записи в таблице указателей. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_Separator](../field/get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_SequenceName](./get_sequencename/)() | Получает имя последовательности, номер которой включён в номер страницы. |
| [get_SequenceSeparator](./get_sequenceseparator/)() | Получает последовательность символов, используемую для разделения номеров последовательностей и номеров страниц. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [get_UseHeading](./get_useheading/)() | Получает, следует ли включать заголовок категории для записей в таблице указателей. |
| [get_UsePassim](./get_usepassim/)() | Получает, следует ли заменять пять и более разных ссылок на страницу к одному и тому же указателю на "passim", что используется для указания того, что слово или отрывок часто встречается в цитируемой работе. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Устанавливает имя закладки, которое отмечает часть документа, используемую для построения таблицы. |
| [set_EntryCategory](./set_entrycategory/)(const System::String\&) | Устанавливает целую категорию для записей, включенных в таблицу. |
| [set_EntrySeparator](./set_entryseparator/)(const System::String\&) | Устанавливает последовательность символов, используемую для разделения записи таблицы указателей и её номера страницы. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PageNumberListSeparator](./set_pagenumberlistseparator/)(const System::String\&) | Устанавливает последовательность символов, используемую для разделения двух номеров страниц в списке номеров страниц. |
| [set_PageRangeSeparator](./set_pagerangeseparator/)(const System::String\&) | Устанавливает последовательность символов, используемую для разделения начала и конца диапазона страниц. |
| [set_RemoveEntryFormatting](./set_removeentryformatting/)(bool) | Устанавливает, следует ли удалять форматирование текста записи в документе из записи в таблице указателей. |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SequenceName](./set_sequencename/)(const System::String\&) | Устанавливает имя последовательности, номер которой включён в номер страницы. |
| [set_SequenceSeparator](./set_sequenceseparator/)(const System::String\&) | Устанавливает последовательность символов, используемую для разделения номеров последовательностей и номеров страниц. |
| [set_UseHeading](./set_useheading/)(bool) | Устанавливает, следует ли включать заголовок категории для записей в таблице указателей. |
| [set_UsePassim](./set_usepassim/)(bool) | Устанавливает, заменять ли пять и более разных ссылок на одну и ту же авторитетную запись на "passim", который используется для указания того, что слово или отрывок встречается часто в цитируемом произведении. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |
## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
