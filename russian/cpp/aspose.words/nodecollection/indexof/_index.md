---
title: "Aspose::Words::NodeCollection::IndexOf метод"
linktitle: "IndexOf"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::NodeCollection::IndexOf метод. Возвращает нулевой индекс указанного узла в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/nodecollection/indexof/
---
## NodeCollection::IndexOf method


Возвращает нулевой индекс указанного узла.

```cpp
int32_t Aspose::Words::NodeCollection::IndexOf(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| узел | const System::SharedPtr\<Aspose::Words::Node\>\& | Узел для поиска. |

### ReturnValue

Нулевой индекс узла в коллекции, если найден; иначе -1.
## Примечания


Этот метод выполняет линейный поиск; поэтому среднее время выполнения пропорционально [Count](../get_count/).

## Примеры



Показывает, как получить индекс узла в коллекции.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::NodeCollection> allTables = doc->GetChildNodes(Aspose::Words::NodeType::Table, true);

ASSERT_EQ(0, allTables->IndexOf(table));

System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(2);

ASSERT_EQ(2, table->IndexOf(row));

System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_LastCell();

ASSERT_EQ(4, row->IndexOf(cell));
```

## См. также

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
