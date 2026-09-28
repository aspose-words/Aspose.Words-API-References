---
title: "Aspose::Words::Fields::FieldDdeAuto класс"
linktitle: "FieldDdeAuto"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldDdeAuto класс. Реализует поле DDEAUTO. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 33000
url: /ru/cpp/aspose.words.fields/fieldddeauto/
---
## FieldDdeAuto class


Реализует поле DDEAUTO. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldDdeAuto : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_InsertAsBitmap](./get_insertasbitmap/)() | Возвращает, следует ли вставлять связанный объект как растровое изображение. |
| [get_InsertAsHtml](./get_insertashtml/)() | Возвращает, следует ли вставлять связанный объект как текст в формате HTML. |
| [get_InsertAsPicture](./get_insertaspicture/)() | Возвращает, следует ли вставлять связанный объект как изображение. |
| [get_InsertAsRtf](./get_insertasrtf/)() | Возвращает, следует ли вставлять связанный объект в формате Rich Text (RTF). |
| [get_InsertAsText](./get_insertastext/)() | Возвращает, следует ли вставлять связанный объект в текстовом формате без разметки. |
| [get_InsertAsUnicode](./get_insertasunicode/)() | Возвращает, следует ли вставлять связанный объект как Unicode‑текст. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLinked](./get_islinked/)() | Возвращает, следует ли уменьшать размер файла, не сохраняя графические данные в документе. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_ProgId](./get_progid/)() | Возвращает тип приложения информации о ссылке. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_Separator](../field/get_separator/)() | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_SourceFullName](./get_sourcefullname/)() | Возвращает имя и расположение исходного файла. |
| [get_SourceItem](./get_sourceitem/)() | Возвращает часть исходного файла, которая связывается. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_InsertAsBitmap](./set_insertasbitmap/)(bool) | Устанавливает, следует ли вставлять связанный объект как растровое изображение. |
| [set_InsertAsHtml](./set_insertashtml/)(bool) | Устанавливает, следует ли вставлять связанный объект как текст в формате HTML. |
| [set_InsertAsPicture](./set_insertaspicture/)(bool) | Устанавливает, следует ли вставлять связанный объект как изображение. |
| [set_InsertAsRtf](./set_insertasrtf/)(bool) | Устанавливает, следует ли вставлять связанный объект в формате Rich Text (RTF). |
| [set_InsertAsText](./set_insertastext/)(bool) | Устанавливает, следует ли вставлять связанный объект в текстовом формате без разметки. |
| [set_InsertAsUnicode](./set_insertasunicode/)(bool) | Устанавливает, следует ли вставлять связанный объект как Unicode‑текст. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLinked](./set_islinked/)(bool) | Устанавливает, следует ли уменьшать размер файла, не сохраняя графические данные в документе. |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_ProgId](./set_progid/)(const System::String\&) | Устанавливает тип приложения для информации о ссылке. |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Устанавливает имя и расположение исходного файла. |
| [set_SourceItem](./set_sourceitem/)(const System::String\&) | Устанавливает часть исходного файла, которая связывается. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |
## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
