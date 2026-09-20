---
title: "Класс Aspose::Words::Fields::FieldNoteRef"
linktitle: "FieldNoteRef"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Fields::FieldNoteRef. Реализует поле NOTEREF. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 72000
url: /ru/cpp/aspose.words.fields/fieldnoteref/
---
## FieldNoteRef class


Реализует поле NOTEREF. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldNoteRef : public Aspose::Words::Fields::Field,
                     public Aspose::Words::Fields::IFieldCodeTokenInfoProvider
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Получает имя закладки. |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_InsertHyperlink](./get_inserthyperlink/)() | Получает, следует ли вставлять гиперссылку на закладочный абзац. |
| [get_InsertReferenceMark](./get_insertreferencemark/)() | Вставляет метку ссылки с тем же форматированием символов, что и стиль ссылки на сноску или конец сноски. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | Получает, следует ли вставлять относительное положение закладочного абзаца. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
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
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | Устанавливает, следует ли вставлять гиперссылку на закладочный абзац. |
| [set_InsertReferenceMark](./set_insertreferencemark/)(bool) | Вставляет метку ссылки с тем же форматированием символов, что и стиль ссылки на сноску или конец сноски. |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | Устанавливает, следует ли вставлять относительное положение закладочного абзаца. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |

## Примеры



Показывает, как делать перекрестные ссылки на сноски с помощью поля NOTEREF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"CrossReference: ");

auto field = System::ExplicitCast<Aspose::Words::Fields::FieldNoteRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldNoteRef, false));
// <--- не обновляйте поле
field->set_BookmarkName(u"CrossRefBookmark");
field->set_InsertHyperlink(true);
field->set_InsertReferenceMark(true);
field->set_InsertRelativePosition(false);
builder->Writeln();

builder->StartBookmark(u"CrossRefBookmark");
builder->Write(u"Hello world!");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Cross referenced footnote.");
builder->EndBookmark(u"CrossRefBookmark");
builder->Writeln();

doc->UpdateFields();

// Это поле работает только в более старых версиях Microsoft Word.
doc->Save(get_ArtifactsDir() + u"Field.NOTEREF.doc");
```

## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
