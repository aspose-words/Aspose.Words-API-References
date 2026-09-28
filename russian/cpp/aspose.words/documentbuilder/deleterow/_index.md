---
title: "Метод Aspose::Words::DocumentBuilder::DeleteRow"
linktitle: "DeleteRow"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::DeleteRow. Удаляет строку из таблицы в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder::DeleteRow method


Удаляет строку из таблицы.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::DocumentBuilder::DeleteRow(int32_t tableIndex, int32_t rowIndex)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| tableIndex | int32_t | Индекс таблицы. |
| rowIndex | int32_t | Индекс строки в таблице. |

### ReturnValue

Узел строки, который только что был удалён.
## Примечания


Если курсор находится внутри строки, которая удаляется, курсор перемещается к следующей строке или к следующему абзацу после таблицы.

Если удалить строку из таблицы, содержащей только одну строку, вся таблица будет удалена.

Для параметров индекса, когда индекс больше или равен 0, он указывает позицию с начала, где 0 — первый элемент. Когда индекс меньше 0, он указывает позицию с конца, где -1 — последний элемент.

## Примеры



Показывает, как удалить строку из таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, cell 2.");
builder->EndTable();

ASSERT_EQ(2, table->get_Rows()->get_Count());

// Удалите первую строку первой таблицы в документе.
builder->DeleteRow(0, 0);

ASSERT_EQ(1, table->get_Rows()->get_Count());
ASSERT_EQ(u"Row 2, cell 1.\aRow 2, cell 2.\a\a", table->GetText().Trim());
```

## См. также

* Class [Row](../../../aspose.words.tables/row/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
