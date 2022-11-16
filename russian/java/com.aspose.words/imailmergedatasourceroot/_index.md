---
title: IMailMergeDataSourceRoot
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, чтобы разрешить слияние почты из пользовательского источника данных с основными и подробными данными.
type: docs
weight: 651
url: /ru/java/com.aspose.words/imailmergedatasourceroot/
---
```
public interface IMailMergeDataSourceRoot
```

Реализуйте этот интерфейс, чтобы разрешить слияние почты из пользовательского источника данных с основными и подробными данными.
## Методы

| Метод | Описание |
| --- | --- |
| [getDataSource(String tableName)](#getDataSource-java.lang.String-) | Механизм слияния почты Aspose.Words вызывает этот метод, когда обнаруживает начало области слияния почты верхнего уровня. |
### getDataSource(String tableName) {#getDataSource-java.lang.String-}
```
public abstract IMailMergeDataSource getDataSource(String tableName)
```


Механизм слияния почты Aspose.Words вызывает этот метод, когда обнаруживает начало области слияния почты верхнего уровня.

Когда механизмы слияния почты Aspose.Words заполняют документ данными и обнаруживают MERGEFIELD TableStart:TableName, он вызывает[getDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasourceroot\#getDataSource-java.lang.String-) на этом объекте. Ваша реализация должна вернуть новый объект источника данных. Aspose.Words будет использовать возвращенный источник данных для заполнения области слияния.

Если источник данных (таблица) с указанным именем не существует, ваша реализация должна вернуть значение null .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| tableName | java.lang.String | Имя региона слияния, указанное в шаблоне документа. Без учета регистра. |

**Возвращает:**
[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) - Объект источника данных, который предоставит доступ к записям данных указанной таблицы.