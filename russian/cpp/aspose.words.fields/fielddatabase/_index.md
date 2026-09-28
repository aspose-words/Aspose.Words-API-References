---
title: "Aspose::Words::Fields::FieldDatabase класс"
linktitle: "FieldDatabase"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldDatabase класс. Реализует поле DATABASE. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 28000
url: /ru/cpp/aspose.words.fields/fielddatabase/
---
## FieldDatabase class


Реализует поле DATABASE. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldDatabase : public Aspose::Words::Fields::Field,
                      public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [FieldDatabase](./fielddatabase/)() |  |
| [get_Connection](./get_connection/)() | Получает соединение с данными. |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_FileName](./get_filename/)() | Получает полный путь и имя файла базы данных. |
| [get_FirstRecord](./get_firstrecord/)() | Получает целый номер первой записи данных для вставки. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_FormatAttributes](./get_formatattributes/)() | Получает, какие атрибуты формата следует применить к таблице. |
| [get_InsertHeadings](./get_insertheadings/)() | Получает, следует ли вставлять имена полей из базы данных в качестве заголовков столбцов в результирующей таблице. |
| [get_InsertOnceOnMailMerge](./get_insertonceonmailmerge/)() | Получает, следует ли вставлять данные в начало слияния. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LastRecord](./get_lastrecord/)() | Получает целый номер последней записи данных для вставки. |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_Query](./get_query/)() | Получает набор инструкций SQL, которые запрашивают базу данных. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_Separator](../field/get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| [get_TableFormat](./get_tableformat/)() | Получает формат, который будет применён к результату запроса к базе данных. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_Connection](./set_connection/)(const System::String\&) | Устанавливает соединение с данными. |
| [set_FileName](./set_filename/)(const System::String\&) | Устанавливает полный путь и имя файла базы данных. |
| [set_FirstRecord](./set_firstrecord/)(const System::String\&) | Устанавливает целый номер первой записи данных для вставки. |
| [set_FormatAttributes](./set_formatattributes/)(const System::String\&) | Устанавливает, какие атрибуты формата следует применить к таблице. |
| [set_InsertHeadings](./set_insertheadings/)(bool) | Устанавливает, следует ли вставлять имена полей из базы данных в качестве заголовков столбцов в результирующей таблице. |
| [set_InsertOnceOnMailMerge](./set_insertonceonmailmerge/)(bool) | Устанавливает, следует ли вставлять данные в начало слияния. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LastRecord](./set_lastrecord/)(const System::String\&) | Устанавливает целый номер последней записи данных для вставки. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Query](./set_query/)(const System::String\&) | Устанавливает набор инструкций SQL, которые запрашивают базу данных. |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_TableFormat](./set_tableformat/)(const System::String\&) | Устанавливает формат, который будет применён к результату запроса к базе данных. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |
## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
