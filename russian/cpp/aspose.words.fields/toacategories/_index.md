---
title: "класс Aspose::Words::Fields::ToaCategories"
linktitle: "ToaCategories"
second_title: "Справочник API Aspose.Words для C++"
description: "класс Aspose::Words::Fields::ToaCategories. Представляет таблицу категорий авторитетов. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 116000
url: /ru/cpp/aspose.words.fields/toacategories/
---
## ToaCategories class


Представляет таблицу категорий авторитетов. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class ToaCategories : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| static [get_DefaultCategories](./get_defaultcategories/)() | Получает таблицу категорий авторитетов по умолчанию. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Получает или задает заголовок категории по номеру категории. |
| [idx_set](./idx_set/)(int32_t, const System::String\&) | Получает или задает заголовок категории по номеру категории. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ToaCategories](./toacategories/)() |  |
| static [Type](./type/)() |  |

## Примеры



Показывает, как указать набор категорий для полей TOA.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Поля TOA могут фильтровать свои записи по категориям, определённым в этой коллекции.
auto toaCategories = System::MakeObject<Aspose::Words::Fields::ToaCategories>();
doc->get_FieldOptions()->set_ToaCategories(toaCategories);

// Эта коллекция категорий поставляется со значениями по умолчанию, которые мы можем переопределить пользовательскими значениями.
ASSERT_EQ(u"Cases", toaCategories->idx_get(1));
ASSERT_EQ(u"Statutes", toaCategories->idx_get(2));

toaCategories->idx_set(1, u"My Category 1");
toaCategories->idx_set(2, u"My Category 2");

// Мы всегда можем получить доступ к значениям по умолчанию через эту коллекцию.
ASSERT_EQ(u"Cases", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(1));
ASSERT_EQ(u"Statutes", Aspose::Words::Fields::ToaCategories::get_DefaultCategories()->idx_get(2));

// Вставьте 2 поля TOA. Поля TOA создают запись для каждого поля TA в документе.
// Используйте переключатель "\c" для выбора индекса категории из нашей коллекции.
//  С этим переключателем поле TOA будет получать записи только из полей TA, которые
// также имеют переключатель "\c" с соответствующим индексом категории. Каждое поле TOA также будет отображать
// название категории, на которую указывает его переключатель "\c".
builder->InsertField(u"TOA \\c 1 \\h", nullptr);
builder->InsertField(u"TOA \\c 2 \\h", nullptr);
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

// Вставьте записи TOA из 2 категорий. Наше первое поле TOA получит одну запись,
// из второго поля TA, чей переключатель "\c" также указывает на первую категорию.
// Второе поле TOA будет иметь две записи из остальных двух полей TA.
builder->InsertField(u"TA \\c 2 \\l \"entry 1\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 1 \\l \"entry 2\"");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->InsertField(u"TA \\c 2 \\l \"entry 3\"");

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"FieldOptions.TOA.Categories.docx");
```

## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
