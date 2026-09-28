---
title: "Aspose::Words::SectionCollection класс"
linktitle: "SectionCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::SectionCollection class. Коллекция объектов Section в документе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 59000
url: /ru/cpp/aspose.words/sectioncollection/
---
## SectionCollection class


Коллекция объектов [Section](../section/) в документе. Чтобы узнать больше, посетите статью документации [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class SectionCollection : public Aspose::Words::NodeCollection
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Добавляет узел в конец коллекции. |
| [Clear](../nodecollection/clear/)() | Удаляет все узлы из этой коллекции и из документа. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Определяет, находится ли узел в коллекции. |
| [get_Count](../nodecollection/get_count/)() | Получает количество узлов в коллекции. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Предоставляет простую итерацию в стиле "foreach" по коллекции узлов. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Получает раздел по заданному индексу. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает нулевой индекс указанного узла. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Вставляет узел в коллекцию по указанному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Удаляет узел из коллекции и из документа. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Удаляет узел по указанному индексу из коллекции и из документа. |
| [ToArray](./toarray/)() | Копирует все разделы из коллекции в новый массив разделов. |
| static [Type](./type/)() |  |
## Примечания


Документ Microsoft Word может содержать несколько разделов. Чтобы создать раздел в Microsoft Word, выберите команду Insert/Break и выберите тип разрыва. Разрыв определяет, начинается ли раздел на новой странице или на той же странице.

Программное вставление и удаление разделов может использоваться для настройки документов, создаваемых при слиянии писем. Если документ должен иметь разное содержание или части содержания в зависимости от некоторых критериев, вы можете создать «главный» документ, содержащий несколько разделов, и удалить некоторые из разделов до или после слияния писем.

## Примеры



Показывает, как добавлять и удалять разделы в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Section 1");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->Write(u"Section 2");

ASSERT_EQ(u"Section 1\x000c" u"Section 2", doc->GetText().Trim());

// Удалите первый раздел из документа.
doc->get_Sections()->RemoveAt(0);

ASSERT_EQ(u"Section 2", doc->GetText().Trim());

// Добавьте копию текущего первого раздела в конец документа.
int32_t lastSectionIdx = doc->get_Sections()->get_Count() - 1;
System::SharedPtr<Aspose::Words::Section> newSection = doc->get_Sections()->idx_get(lastSectionIdx)->Clone();
doc->get_Sections()->Add(newSection);

ASSERT_EQ(u"Section 2\x000c" u"Section 2", doc->GetText().Trim());
```

## См. также

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
