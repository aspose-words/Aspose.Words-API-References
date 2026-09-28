---
title: "Метод Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult"
linktitle: "GetQueryResult"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult. Возвращает результат запроса в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider::GetQueryResult method


Возвращает результат запроса.

```cpp
virtual System::SharedPtr<Aspose::Words::Fields::FieldDatabaseDataTable> Aspose::Words::Fields::IFieldDatabaseProvider::GetQueryResult(System::String fileName, System::String connection, System::String query, System::SharedPtr<Aspose::Words::Fields::FieldDatabase> field)=0
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | System::String | Полный путь и имя файла базы данных, указанные в переключателе поля \d. |
| connection | System::String | Подключение к данным, указанным в переключателе поля \c. |
| запрос | System::String | Набор SQL‑инструкций, которые запрашивают базу данных, указанную в переключателе поля \\s. |
| поле | System::SharedPtr\\<Aspose::Words::Fields::FieldDatabase\\> | Поле, которое обновляется. |

### ReturnValue

Экземпляр [FieldDatabaseDataTable](../../fielddatabasedatatable/), который следует использовать для обновления поля.

## См. также

* Class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* Class [FieldDatabase](../../fielddatabase/)
* Interface [IFieldDatabaseProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
