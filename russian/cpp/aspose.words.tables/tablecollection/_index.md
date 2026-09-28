---
title: "Aspose::Words::Tables::TableCollection класс"
linktitle: "TableCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::TableCollection класс. Предоставляет типизированный доступ к коллекции узлов Table. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.tables/tablecollection/
---
## TableCollection class


Предоставляет типизированный доступ к коллекции узлов [Table](../table/). Чтобы узнать больше, посетите статью документации [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class TableCollection : public Aspose::Words::NodeCollection
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Добавляет узел в конец коллекции. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Удаляет все узлы из этой коллекции и из документа. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Определяет, находится ли узел в коллекции. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Получает количество узлов в коллекции. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Предоставляет простую итерацию в стиле "foreach" по коллекции узлов. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Получает [Table](../table/) по заданному индексу. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает нулевой индекс указанного узла. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Вставляет узел в коллекцию по указанному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Удаляет узел из коллекции и из документа. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Удаляет узел по указанному индексу из коллекции и из документа. |
| [ToArray](./toarray/)() | Копирует все таблицы из коллекции в новый массив таблиц. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как удалить первую и последнюю строки во всех таблицах документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(5, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(4, tables->idx_get(1)->get_Rows()->get_Count());

for (auto&& table : System::IterateOver(tables->LINQ_OfType<System::SharedPtr<Aspose::Words::Tables::Table> >()))
{
    System::SharedPtr<Aspose::Words::Tables::Row> condExpression = table->get_FirstRow();
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }
    System::SharedPtr<Aspose::Words::Tables::Row> condExpression2 = table->get_LastRow();
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }
}

ASSERT_EQ(3, tables->idx_get(0)->get_Rows()->get_Count());
ASSERT_EQ(2, tables->idx_get(1)->get_Rows()->get_Count());
```

## См. также

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
