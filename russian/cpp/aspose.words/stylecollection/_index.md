---
title: "Aspose::Words::StyleCollection класс"
linktitle: "StyleCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::StyleCollection класс. Коллекция объектов Style, представляющих как встроенные, так и пользовательские стили в документе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 65000
url: /ru/cpp/aspose.words/stylecollection/
---
## StyleCollection class


Коллекция объектов [Style](../style/), представляющих как встроенные, так и пользовательские стили в документе. Чтобы узнать больше, посетите статью документации [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class StyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Style>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](./add/)(Aspose::Words::StyleType, const System::String\&) | Создает новый пользовательский стиль и добавляет его в коллекцию. |
| [AddCopy](./addcopy/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | Копирует стиль в эту коллекцию. |
| [ClearQuickStyleGallery](./clearquickstylegallery/)() | Удаляет все стили из быстрой панели галереи [Style](../style/). |
| [get_Count](./get_count/)() | Получает количество стилей в коллекции. |
| [get_DefaultFont](./get_defaultfont/)() | Получает форматирование текста по умолчанию документа. |
| [get_DefaultParagraphFormat](./get_defaultparagraphformat/)() | Получает форматирование абзаца по умолчанию документа. |
| [get_Document](./get_document/)() const | Получает документ‑владельца. |
| [GetEnumerator](./getenumerator/)() override | Получает объект‑перечислитель, который перечисляет стили в алфавитном порядке их имен. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(const System::String\&) | Получает стиль по имени или псевдониму. |
| [idx_get](./idx_get/)(Aspose::Words::StyleIdentifier) | Получает встроенный стиль по его независимому от локали идентификатору. |
| [idx_get](./idx_get/)(int32_t) | Получает стиль по индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Примеры



Показывает, как создать и использовать абзацный стиль со списковой разметкой.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте пользовательский абзацный стиль.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// Создайте список и убедитесь, что абзацы, использующие этот стиль, будут использовать этот список.
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// Примените абзацный стиль к текущему абзацу DocumentBuilder, а затем добавьте некоторый текст.
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// Измените стиль DocumentBuilder на такой, который не содержит форматирования списка, и напишите еще один абзац.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
