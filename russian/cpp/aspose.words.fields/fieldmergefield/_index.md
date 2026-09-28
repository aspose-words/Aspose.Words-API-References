---
title: "Aspose::Words::Fields::FieldMergeField class"
linktitle: "FieldMergeField"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldMergeField class. Реализует поле MERGEFIELD. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 67000
url: /ru/cpp/aspose.words.fields/fieldmergefield/
---
## FieldMergeField class


Реализует поле MERGEFIELD. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldMergeField : public Aspose::Words::Fields::Field,
                        public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldName](./get_fieldname/)() | Получает имя поля данных. |
| [get_FieldNameNoPrefix](./get_fieldnamenoprefix/)() const | Возвращает только имя поля данных. Любой префикс удаляется в свойстве prefix. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_IsMapped](./get_ismapped/)() | Получает, является ли это поле сопоставленным полем. |
| [get_IsVerticalFormatting](./get_isverticalformatting/)() | Получает, включено ли преобразование символов для вертикального форматирования. |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_Separator](../field/get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| [get_TextAfter](./get_textafter/)() | Получает текст, который будет вставлен после поля, если поле не пустое. |
| [get_TextBefore](./get_textbefore/)() | Получает текст, который будет вставлен перед полем, если поле не пустое. |
| [get_Type](./get_type/)() const override | Получает тип поля Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_FieldName](./set_fieldname/)(const System::String\&) | Устанавливает имя поля данных. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_IsMapped](./set_ismapped/)(bool) | Устанавливает, является ли это поле сопоставленным полем. |
| [set_IsVerticalFormatting](./set_isverticalformatting/)(bool) | Устанавливает, включено ли преобразование символов для вертикального форматирования. |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_TextAfter](./set_textafter/)(const System::String\&) | Устанавливает текст, который будет вставлен после поля, если поле не пустое. |
| [set_TextBefore](./set_textbefore/)(const System::String\&) | Устанавливает текст, который будет вставлен перед полем, если поле не пустое. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |
## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
