---
title: "Класс Aspose::Words::Range"
linktitle: "Диапазон"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Range. Представляет непрерывную область в документе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 51000
url: /ru/cpp/aspose.words/range/
---
## Range class


Представляет непрерывную область в документе. Чтобы узнать больше, посетите статью документации [Working with Ranges](https://docs.aspose.com/words/cpp/working-with-ranges/).

```cpp
class Range : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [Delete](./delete/)() | Удаляет все символы диапазона. |
| [get_Bookmarks](./get_bookmarks/)() | Возвращает коллекцию [Bookmarks](./get_bookmarks/), представляющую все закладки в диапазоне. |
| [get_Fields](./get_fields/)() | Возвращает коллекцию [Fields](./get_fields/), представляющую все поля в диапазоне. |
| [get_FormFields](./get_formfields/)() | Возвращает коллекцию [FormFields](./get_formfields/), представляющую все поля формы в диапазоне. |
| [get_Revisions](./get_revisions/)() | Получает коллекцию исправлений (отслеживаемых изменений), существующих в этом диапазоне. |
| [get_StructuredDocumentTags](./get_structureddocumenttags/)() | Возвращает коллекцию [StructuredDocumentTags](./get_structureddocumenttags/), представляющую все структурированные теги документа в диапазоне. |
| [get_Text](./get_text/)() | Получает текст диапазона. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Изменяет значения типа поля [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) у [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/) и [FieldEnd](../../aspose.words.fields/fieldend/) в этом диапазоне, чтобы они соответствовали типам полей, содержащимся в кодах полей. |
| [Replace](./replace/)(const System::String\&, const System::String\&) | Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Заменяет все вхождения шаблона символов, указанного регулярным выражением, другой строкой. |
| [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Заменяет все вхождения указанного шаблона строкового символа на строку‑заменитель. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Заменяет все вхождения шаблона символов, указанного регулярным выражением, другой строкой. |
| [ToDocument](./todocument/)() | Создаёт новый полностью сформированный документ, содержащий диапазон. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Отсоединяет поля в этом диапазоне. |
| [UpdateFields](./updatefields/)() | Обновляет значения полей документа в этом диапазоне. |
## Примечания


Документ представлен в виде дерева узлов, и узлы предоставляют операции для работы с деревом, но некоторые операции проще выполнять, если документ рассматривается как непрерывная последовательность текста.

[Range](./) is a "facade" interface that provide methods that treat the document or portions of the document as "flat" text regardless of the fact that the document nodes are stored in a tree-like object model.

[Range](./) does not contain any text or nodes, it is merely a view or "window" over a fragment of a document.

## Примеры



Показывает, как получить текстовое содержимое всех узлов, охватываемых диапазоном.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
