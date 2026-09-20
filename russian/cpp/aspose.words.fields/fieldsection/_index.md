---
title: "Aspose::Words::Fields::FieldSection класс"
linktitle: "FieldSection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldSection класс. Реализует поле SECTION. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 88000
url: /ru/cpp/aspose.words.fields/fieldsection/
---
## FieldSection class


Реализует поле SECTION. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldSection : public Aspose::Words::Fields::Field
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
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
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |

## Примеры



Показывает, как использовать поля SECTION и SECTIONPAGES для нумерации страниц по разделам.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);

// Поле SECTION отображает номер раздела, в котором оно находится.
builder->Write(u"Section ");
auto fieldSection = System::ExplicitCast<Aspose::Words::Fields::FieldSection>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSection, true));

ASSERT_EQ(u" SECTION ", fieldSection->GetFieldCode());

// Поле PAGE отображает номер страницы, в которой оно находится.
builder->Write(u"\nPage ");
auto fieldPage = System::ExplicitCast<Aspose::Words::Fields::FieldPage>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPage, true));

ASSERT_EQ(u" PAGE ", fieldPage->GetFieldCode());

// Поле SECTIONPAGES отображает количество страниц, охватываемых разделом, в котором оно находится.
builder->Write(u" of ");
auto fieldSectionPages = System::ExplicitCast<Aspose::Words::Fields::FieldSectionPages>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSectionPages, true));

ASSERT_EQ(u" SECTIONPAGES ", fieldSectionPages->GetFieldCode());

// Выйдите из верхнего колонтитула обратно в основной документ и вставьте две страницы.
// Все эти страницы будут в первом разделе. Наши поля, которые появляются в каждом верхнем колонтитуле,
// будут нумеровать текущие/общие страницы этого раздела.
builder->MoveToDocumentEnd();
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Мы можем вставить новый раздел с помощью Document Builder следующим образом.
// Это повлияет на значения, отображаемые в полях SECTION и SECTIONPAGES во всех последующих верхних колонтитулах.
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

// Поле PAGE будет продолжать подсчитывать страницы по всему документу.
// Мы можем вручную сбрасывать его счётчик в каждом разделе, чтобы отслеживать страницы по разделам.
builder->get_CurrentSection()->get_PageSetup()->set_RestartPageNumbering(true);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.SECTION.SECTIONPAGES.docx");
```

## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
