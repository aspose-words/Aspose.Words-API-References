---
title: "Aspose::Words::Fields::FieldBibliography класс"
linktitle: "FieldBibliography"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldBibliography класс. Реализует поле BIBLIOGRAPHY. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 18000
url: /ru/cpp/aspose.words.fields/fieldbibliography/
---
## FieldBibliography class


Реализует поле BIBLIOGRAPHY. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldBibliography : public Aspose::Words::Fields::Field,
                          public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_FilterLanguageId](./get_filterlanguageid/)() | Получает идентификатор языка, который используется для фильтрации библиографических данных, оставляя только источники в документе, использующие этот язык. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_FormatLanguageId](./get_formatlanguageid/)() | Получает идентификатор языка, который используется для форматирования библиографических источников в документе. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_Separator](../field/get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_SourceTag](./get_sourcetag/)() | Получает значение, чтобы в библиографии отображались только источники с соответствующим значением элемента Tag. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_FilterLanguageId](./set_filterlanguageid/)(const System::String\&) | Устанавливает идентификатор языка, который используется для фильтрации библиографических данных, оставляя только источники в документе, использующие этот язык. |
| [set_FormatLanguageId](./set_formatlanguageid/)(const System::String\&) | Устанавливает идентификатор языка, который используется для форматирования библиографических источников в документе. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceTag](./set_sourcetag/)(const System::String\&) | Устанавливает значение, чтобы в библиографии отображались только источники с соответствующим значением элемента Tag. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |
## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
