---
title: "Aspose::Words::Fields::FieldRef класс"
linktitle: "FieldRef"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldRef класс. Реализует поле REF. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 85000
url: /ru/cpp/aspose.words.fields/fieldref/
---
## FieldRef class


Реализует поле REF. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldRef : public Aspose::Words::Fields::Field,
                 public Aspose::Words::Fields::IFieldCodeTokenInfoProvider,
                 public Aspose::Words::Fields::IMergeFieldSurrogate
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_BookmarkName](./get_bookmarkname/)() | Получает или задает имя ссылочной закладки. |
| [get_DisplayResult](../field/get_displayresult/)() | Получает текст, представляющий отображаемый результат поля. |
| [get_End](./get_end/)() override | Получает узел, представляющий конец поля. |
| [get_End](../field/get_end/)() const | Получает узел, представляющий конец поля. |
| [get_FieldEnd](../field/get_fieldend/)() const | Получает узел, представляющий конец поля. |
| [get_FieldStart](../field/get_fieldstart/)() const | Получает узел, представляющий начало поля. |
| [get_Format](../field/get_format/)() | Получает объект [FieldFormat](../fieldformat/), который предоставляет типизированный доступ к форматированию поля. |
| [get_IncludeNoteOrComment](./get_includenoteorcomment/)() | Получает, следует ли увеличивать номера сносок, концевых сносок и аннотаций, отмеченных закладкой, и вставлять соответствующий текст сноски, концевой сноски и комментария. |
| [get_InsertHyperlink](./get_inserthyperlink/)() | Получает, следует ли создавать гиперссылку на закладочный абзац. |
| [get_InsertParagraphNumber](./get_insertparagraphnumber/)() | Получает, следует ли вставлять номер абзаца ссылочного абзаца точно так, как он отображается в документе. |
| [get_InsertParagraphNumberInFullContext](./get_insertparagraphnumberinfullcontext/)() | Получает, следует ли вставлять номер абзаца ссылочного абзаца в полном контексте. |
| [get_InsertParagraphNumberInRelativeContext](./get_insertparagraphnumberinrelativecontext/)() | Получает, следует ли вставлять номер абзаца ссылочного абзаца в относительном контексте. |
| [get_InsertRelativePosition](./get_insertrelativeposition/)() | Получает, следует ли вставлять относительное положение ссылочного абзаца. |
| [get_IsDirty](../field/get_isdirty/)() | Получает или задает, является ли текущий результат поля более некорректным (устаревшим) из‑за других изменений, внесённых в документ. |
| [get_IsLocked](../field/get_islocked/)() | Получает или задает, заблокировано ли поле (не должно пересчитывать свой результат). |
| [get_LocaleId](../field/get_localeid/)() | Получает или задает LCID поля. |
| [get_NumberSeparator](./get_numberseparator/)() | Получает последовательность символов, используемую для разделения номеров последовательностей и номеров страниц. |
| [get_Result](../field/get_result/)() | Получает или задает текст, находящийся между разделителем поля и его концом. |
| [get_Separator](./get_separator/)() override | Получает узел, представляющий разделитель поля. Может быть **null**. |
| [get_Start](./get_start/)() override | Получает узел, представляющий начало поля. |
| [get_Start](../field/get_start/)() const | Получает узел, представляющий начало поля. |
| [get_SuppressNonDelimiters](./get_suppressnondelimiters/)() | Получает, следует ли подавлять символы, не являющиеся разделителями. |
| virtual [get_Type](../field/get_type/)() const | Получает тип поля Microsoft Word. |
| [GetFieldCode](../field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). Включены как код поля, так и результат дочерних полей. |
| [GetFieldCode](../field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделитель отсутствует). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Remove](../field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает родительский абзац. Если поле уже удалено, возвращает **null**. |
| [set_BookmarkName](./set_bookmarkname/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::FieldRef::get_BookmarkName](./get_bookmarkname/). |
| [set_IncludeNoteOrComment](./set_includenoteorcomment/)(bool) | Задает, следует ли увеличивать номера сносок, концевых сносок и аннотаций, отмеченных закладкой, и вставлять соответствующий текст сноски, концевой сноски и комментария. |
| [set_InsertHyperlink](./set_inserthyperlink/)(bool) | Задает, следует ли создавать гиперссылку на закладочный абзац. |
| [set_InsertParagraphNumber](./set_insertparagraphnumber/)(bool) | Задает, следует ли вставлять номер абзаца ссылочного абзаца точно так, как он отображается в документе. |
| [set_InsertParagraphNumberInFullContext](./set_insertparagraphnumberinfullcontext/)(bool) | Задает, следует ли вставлять номер абзаца ссылочного абзаца в полном контексте. |
| [set_InsertParagraphNumberInRelativeContext](./set_insertparagraphnumberinrelativecontext/)(bool) | Устанавливает, следует ли вставлять номер абзаца ссылочного абзаца в относительном контексте. |
| [set_InsertRelativePosition](./set_insertrelativeposition/)(bool) | Устанавливает, следует ли вставлять относительное положение ссылочного абзаца. |
| [set_IsDirty](../field/set_isdirty/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsDirty](../field/get_isdirty/). |
| [set_IsLocked](../field/set_islocked/)(bool) | Сеттер для [Aspose::Words::Fields::Field::get_IsLocked](../field/get_islocked/). |
| [set_LocaleId](../field/set_localeid/)(int32_t) | Сеттер для [Aspose::Words::Fields::Field::get_LocaleId](../field/get_localeid/). |
| [set_NumberSeparator](./set_numberseparator/)(const System::String\&) | Устанавливает последовательность символов, используемую для разделения номеров последовательностей и номеров страниц. |
| [set_Result](../field/set_result/)(const System::String\&) | Сеттер для [Aspose::Words::Fields::Field::get_Result](../field/get_result/). |
| [set_SuppressNonDelimiters](./set_suppressnondelimiters/)(bool) | Устанавливает, следует ли подавлять неделительные символы. |
| static [Type](./type/)() |  |
| [Unlink](../field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../field/update/)() | Выполняет обновление поля. Вызывает исключение, если поле уже обновляется. |
| [Update](../field/update/)(bool) | Выполняет обновление поля. Выбрасывает исключение, если поле уже обновляется. |

## Примеры



Показывает, как создать текст с закладкой с помощью поля SET, а затем отобразить его в документе с помощью поля REF.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Назовите текст с закладкой с помощью поля SET.
// Это поле ссылается на \"bookmark\", а не на структуру закладки, которая появляется в тексте, а на именованную переменную.
auto fieldSet = System::ExplicitCast<Aspose::Words::Fields::FieldSet>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldSet, false));
fieldSet->set_BookmarkName(u"MyBookmark");
fieldSet->set_BookmarkText(u"Hello world!");
fieldSet->Update();

ASSERT_EQ(u" SET  MyBookmark \"Hello world!\"", fieldSet->GetFieldCode());

// Обратитесь к закладке по имени в поле REF и отобразите её содержимое.
auto fieldRef = System::ExplicitCast<Aspose::Words::Fields::FieldRef>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldRef, true));
fieldRef->set_BookmarkName(u"MyBookmark");
fieldRef->Update();

ASSERT_EQ(u" REF  MyBookmark", fieldRef->GetFieldCode());
ASSERT_EQ(u"Hello world!", fieldRef->get_Result());

doc->Save(get_ArtifactsDir() + u"Field.SET.REF.docx");
```

## См. также

* Class [Field](../field/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
