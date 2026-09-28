---
title: "Aspose::Words::Fields::FieldPage class"
linktitle: "FieldPage"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldPage class. Реализует поле PAGE. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 78000
url: /ru/cpp/aspose.words.fields/fieldpage/
---
## FieldPage class


Реализует поле PAGE. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldPage : public Aspose::Words::Fields::Field
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



Показывает, как использовать поля NUMCHARS, NUMWORDS, NUMPAGES и PAGE для отслеживания размера наших документов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::FooterPrimary);
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

// Ниже представлены три типа полей, которые мы можем использовать для отслеживания размера наших документов.
// 1 -  Отслеживайте количество символов с помощью поля NUMCHARS:
auto fieldNumChars = System::ExplicitCast<Aspose::Words::Fields::FieldNumChars>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldNumChars, true));
builder->Writeln(u" characters");

// 2 -  Отслеживайте количество слов с помощью поля NUMWORDS:
auto fieldNumWords = System::ExplicitCast<Aspose::Words::Fields::FieldNumWords>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldNumWords, true));
builder->Writeln(u" words");

// 3 -  Используйте поля PAGE и NUMPAGES вместе, чтобы отобразить, на какой странице находится поле,
// и общее количество страниц в документе:
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);
builder->Write(u"Page ");
auto fieldPage = System::ExplicitCast<Aspose::Words::Fields::FieldPage>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldPage, true));
builder->Write(u" of ");
auto fieldNumPages = System::ExplicitCast<Aspose::Words::Fields::FieldNumPages>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldNumPages, true));

ASSERT_EQ(u" NUMCHARS ", fieldNumChars->GetFieldCode());
ASSERT_EQ(u" NUMWORDS ", fieldNumWords->GetFieldCode());
ASSERT_EQ(u" NUMPAGES ", fieldNumPages->GetFieldCode());
ASSERT_EQ(u" PAGE ", fieldPage->GetFieldCode());

// Эти поля не будут поддерживать точные значения в реальном времени
// пока мы редактируем документ программно с помощью Aspose.Words или в Microsoft Word.
// Нам нужно обновлять их каждый раз, когда требуется увидеть актуальное значение.
doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.NUMCHARS.NUMWORDS.NUMPAGES.PAGE.docx");
```

## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
