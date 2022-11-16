---
title: IMailMergeDataSource
second_title: Справочник по API Aspose.Words для Java
description: Реализуйте этот интерфейс, чтобы разрешить слияние почты из пользовательского источника данных, такого как список объектов.
type: docs
weight: 650
url: /ru/java/com.aspose.words/imailmergedatasource/
---
```
public interface IMailMergeDataSource
```

Реализуйте этот интерфейс, чтобы разрешить слияние почты из пользовательского источника данных, например списка объектов. Данные Master-Detail также поддерживаются.

При создании источника данных его следует инициализировать, чтобы он указывал на BOF (перед первой записью). Механизм слияния почты Aspose.Words вызовет[moveNext()](../../com.aspose.words/imailmergedatasource\#moveNext--) чтобы перейти к следующей записи, а затем вызвать**M:Aspose.Words.MailMerging.IMailMergeDataSource.GetValue(System.String,System.Object@)** для каждого поля слияния, которое встречается в документе или в текущей области слияния.
## Методы

| Метод | Описание |
| --- | --- |
| [getChildDataSource(String tableName)](#getChildDataSource-java.lang.String-) | Механизм слияния почты Aspose.Words вызывает этот метод, когда обнаруживает начало вложенной области слияния. |
| [getTableName()](#getTableName--) | Возвращает имя источника данных. |
| [getValue(String fieldName, Ref fieldValue)](#getValue-java.lang.String-com.aspose.words.ref.Ref-) |  |
| [moveNext()](#moveNext--) | Переход к следующей записи в источнике данных. |
### getChildDataSource(String tableName) {#getChildDataSource-java.lang.String-}
```
public abstract IMailMergeDataSource getChildDataSource(String tableName)
```


Механизм слияния почты Aspose.Words вызывает этот метод, когда обнаруживает начало вложенной области слияния.

 Когда механизмы слияния почты Aspose.Words заполняют область слияния данными и обнаруживают начало вложенной области слияния в форме MERGEFIELD TableStart:TableName, он вызывает[getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource\#getChildDataSource-java.lang.String-) на текущем объекте источника данных. Ваша реализация должна вернуть новый объект источника данных, который обеспечит доступ к дочерним записям текущей родительской записи. Aspose.Words будет использовать возвращенный источник данных для заполнения вложенной области слияния.

Ниже приведены правила, выполнение которых[getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource\#getChildDataSource-java.lang.String-) должен следовать.

 Если таблица, представленная этим объектом источника данных, имеет связанную дочернюю (подробную) таблицу с указанным именем, то ваша реализация должна вернуть новый[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) объект, который предоставит доступ к дочерним записям текущей записи. Примером этого является отношение Orders / OrderDetails. Предположим, что текущий[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) Объект представляет таблицу Orders и имеет текущую запись заказа. Затем Aspose.Words встречает в документе «MERGEFIELD TableStart:OrderDetails» и вызывает[getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource\#getChildDataSource-java.lang.String-) . Вам нужно создать и вернуть[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) объект, который позволит Aspose.Words получить доступ к записи OrderDetails для текущего заказа.

 Если этот объект источника данных не имеет отношения к таблице с указанным именем, то необходимо вернуть[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) объект, который предоставит доступ ко всем записям указанной таблицы.

Если таблица с указанным именем не существует, ваша реализация должна вернуть значение null .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| tableName | java.lang.String | Имя региона слияния, указанное в шаблоне документа. Без учета регистра. |

**Возвращает:**
[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) - Объект источника данных, который предоставит доступ к записям данных указанной таблицы.
### getTableName() {#getTableName--}
```
public abstract String getTableName()
```


Возвращает имя источника данных.

 Если вы реализуете[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource), верните имя источника данных из этого свойства.

Aspose.Words использует это имя для сопоставления с именем региона слияния, указанным в шаблоне документа. При сравнении имени источника данных и имени региона слияния не учитывается регистр.

**Возвращает:**
java.lang.String — имя источника данных. Пустая строка, если у источника данных нет имени.
### getValue(String fieldName, Ref fieldValue) {#getValue-java.lang.String-com.aspose.words.ref.Ref-}
```
public abstract boolean getValue(String fieldName, Ref fieldValue)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldName | java.lang.String |  |
| fieldValue | [Ref](../../com.aspose.words.ref/ref) |  |

**Возвращает:**
логический
### moveNext() {#moveNext--}
```
public abstract boolean moveNext()
```


Переход к следующей записи в источнике данных.

**Возвращает:**
boolean — Истинно, если успешно перенесено на следующую запись. False, если достигнут конец источника данных.