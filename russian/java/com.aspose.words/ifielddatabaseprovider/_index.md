---
title: IFieldDatabaseProvider
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс для предоставления данных для поля при его обновлении.
type: docs
weight: 640
url: /ru/java/com.aspose.words/ifielddatabaseprovider/
---
```
public interface IFieldDatabaseProvider
```

 Реализуйте этот интерфейс для предоставления данных для[FieldDatabase](../../com.aspose.words/fielddatabase)поле, когда оно обновляется.
## Методы

| Метод | Описание |
| --- | --- |
| [getQueryResult(String fileName, String connection, String query, FieldDatabase field)](#getQueryResult-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.FieldDatabase-) | Возвращает результат запроса. |
### getQueryResult(String fileName, String connection, String query, FieldDatabase field) {#getQueryResult-java.lang.String-java.lang.String-java.lang.String-com.aspose.words.FieldDatabase-}
```
public abstract FieldDatabaseDataTable getQueryResult(String fileName, String connection, String query, FieldDatabase field)
```


Возвращает результат запроса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String |  Полный путь и имя файла базы данных, указанные в\Переключатель поля \d. |
| connection | java.lang.String |  Связь с данными, указанными в\Переключатель поля \c. |
| query | java.lang.String |  Набор инструкций SQL, которые запрашивают базу данных, указанную в\Переключатель поля \s. |
| field | [FieldDatabase](../../com.aspose.words/fielddatabase) | Поле обновляется. |

**Возвращает:**
[FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable) -[FieldDatabaseDataTable](../../com.aspose.words/fielddatabasedatatable) экземпляр, который следует использовать для обновления поля.