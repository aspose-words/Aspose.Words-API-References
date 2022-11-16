---
title: IDataRecord
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет доступ к значениям столбца в каждой строке для DataReader и реализуется поставщиками данных .NET Framework, которые обращаются к реляционным базам данных.
type: docs
weight: 35
url: /ru/java/com.aspose.words.net.system.data/idatarecord/
---
```
public interface IDataRecord
```

Предоставляет доступ к значениям столбцов в каждой строке для DataReader и реализуется поставщиками данных .NET Framework, которые обращаются к реляционным базам данных.
## Методы

| Метод | Описание |
| --- | --- |
| [get(int i)](#get-int-) | Получает столбец, расположенный по указанному индексу. |
| [getFieldCount()](#getFieldCount--) | Получает количество столбцов в текущей строке. |
| [getFieldType(int i)](#getFieldType-int-) |  Получает информацию java.lang.Class, соответствующую типу java.lang.Object, который будет возвращен из[getValue(int)](../../com.aspose.words.net.system.data/idatarecord\#getValue-int-). |
| [getName(int i)](#getName-int-) | Получает имя поля для поиска. |
| [getValue(int i)](#getValue-int-) | Возвращает значение указанного поля. |
### get(int i) {#get-int-}
```
public abstract Object get(int i)
```


Получает столбец, расположенный по указанному индексу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| i | int | Отсчитываемый от нуля индекс столбца, который требуется получить. |

**Возвращает:**
java.lang.Object — столбец, расположенный по указанному индексу как java.lang.Object.
### getFieldCount() {#getFieldCount--}
```
public abstract int getFieldCount()
```


Получает количество столбцов в текущей строке.

**Возвращает:**
int — если не находится в допустимом наборе записей, 0; в противном случае количество столбцов в текущей записи. По умолчанию -1.
### getFieldType(int i) {#getFieldType-int-}
```
public abstract Class getFieldType(int i)
```


 Получает информацию java.lang.Class, соответствующую типу java.lang.Object, который будет возвращен из[getValue(int)](../../com.aspose.words.net.system.data/idatarecord\#getValue-int-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| i | int | Индекс поля для поиска. |

**Возвращает:**
 java.lang.Class — информация java.lang.Class, соответствующая типу java.lang.Object, который будет возвращен из[getValue(int)](../../com.aspose.words.net.system.data/idatarecord\#getValue-int-).
### getName(int i) {#getName-int-}
```
public abstract String getName(int i)
```


Получает имя поля для поиска.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| i | int | Индекс поля для поиска. |

**Возвращает:**
java.lang.String — имя поля или пустая строка (""), если нет возвращаемого значения.
### getValue(int i) {#getValue-int-}
```
public abstract Object getValue(int i)
```


Возвращает значение указанного поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| i | int | Индекс поля для поиска. |

**Возвращает:**
java.lang.Object — объект java.lang.Object, который будет содержать значение поля по возвращении.