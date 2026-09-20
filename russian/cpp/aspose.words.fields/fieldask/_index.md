---
title: "Aspose::Words::Fields::FieldAsk класс"
linktitle: "FieldAsk"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldAsk класс. Реализует поле ASK. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.fields/fieldask/
---
## FieldAsk class


Реализует поле ASK. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldAsk : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Получает имя закладки. |
| [get_DefaultResponse](./get_defaultresponse/)() | Получает ответ пользователя по умолчанию (начальное значение, содержащееся в окне подсказки). |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_PromptOnceOnMailMerge](./get_promptonceonmailmerge/)() | Получает, должен ли ответ пользователя получаться один раз за операцию слияния почты. |
| [get_PromptText](./get_prompttext/)() | Получает текст подсказки (заголовок окна подсказки). |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_Separator](../field/get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Устанавливает имя закладки. |
| [set_DefaultResponse](./set_defaultresponse/)(const System::String\&) | Устанавливает ответ пользователя по умолчанию (начальное значение, содержащееся в окне подсказки). |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_PromptOnceOnMailMerge](./set_promptonceonmailmerge/)(bool) | Устанавливает, следует ли получать ответ пользователя один раз за операцию слияния почты. |
| [set_PromptText](./set_prompttext/)(const System::String\&) | Устанавливает текст подсказки (заголовок окна подсказки). |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |
## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
