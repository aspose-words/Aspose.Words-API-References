---
title: IFieldDatabaseProvider.GetQueryResult
linktitle: GetQueryResult
articleTitle: GetQueryResult
second_title: Aspose.Words для .NET
description: IFieldDatabaseProvider GetQueryResult метод. Возвращает результат запроса на С#.
type: docs
weight: 10
url: /ru/net/aspose.words.fields/ifielddatabaseprovider/getqueryresult/
---
## IFieldDatabaseProvider.GetQueryResult method

Возвращает результат запроса.

```csharp
public FieldDatabaseDataTable GetQueryResult(string fileName, string connection, string query, 
    FieldDatabase field)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | String | Полный путь и имя файла базы данных, указанные в переключателе поля \d. |
| connection | String | Соединение с данными, указанными в переключателе поля \c. |
| query | String | Набор инструкций SQL, которые запрашивают базу данных, указанную в переключателе поля \s. |
| field | FieldDatabase | Поле обновляется. |

### Возвращаемое значение

[`FieldDatabaseDataTable`](../../fielddatabasedatatable/) экземпляр, который следует использовать для обновления поля.

### Смотрите также

* class [FieldDatabaseDataTable](../../fielddatabasedatatable/)
* class [FieldDatabase](../../fielddatabase/)
* interface [IFieldDatabaseProvider](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
