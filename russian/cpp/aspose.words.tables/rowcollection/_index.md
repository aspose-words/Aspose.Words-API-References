---
title: "Aspose::Words::Tables::RowCollection класс"
linktitle: "RowCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::RowCollection класс. Предоставляет типизированный доступ к коллекции узлов Row. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.tables/rowcollection/
---
## RowCollection class


Предоставляет типизированный доступ к коллекции узлов [Row](../row/). Чтобы узнать больше, посетите статью документации [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class RowCollection : public Aspose::Words::NodeCollection
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
| [idx_get](./idx_get/)(int32_t) | Получает [Row](../row/) по заданному индексу. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает нулевой индекс указанного узла. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Вставляет узел в коллекцию по указанному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Удаляет узел из коллекции и из документа. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Удаляет узел по указанному индексу из коллекции и из документа. |
| [ToArray](./toarray/)() | Копирует все строки из коллекции в новый массив строк. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как пройтись по всем таблицам в документе и вывести содержимое каждой ячейки.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // Мы можем использовать метод "ToArray" для коллекции строк, чтобы клонировать её в массив.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // Мы можем использовать метод "ToArray" для коллекции ячеек, чтобы клонировать её в массив.
        ASPOSE_ASSERT_EQ(cells, cells->ToArray());
        ASPOSE_ASSERT_NS(cells, cells->ToArray());

        for (int32_t k = 0; k < cells->get_Count(); k++)
        {
            System::String cellText = cells->idx_get(k)->ToString(Aspose::Words::SaveFormat::Text).Trim();
            std::cout << System::String::Format(u"\t\tContents of Cell:{0} = \"{1}\"", k, cellText) << std::endl;
        }

        std::cout << System::String::Format(u"\tEnd of Row {0}", j) << std::endl;
    }

    std::cout << System::String::Format(u"End of Table {0}\n", i) << std::endl;
}
```

## См. также

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
